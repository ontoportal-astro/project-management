# OntoPortal-Astro VM Documentation

## 1. Users in the Virtual Machine

The VM includes the following users:

- **root**: Administrative user with full access.
- **ontoportal**: The main user for managing all services and projects is ontoportal.
- **ubuntu**: Default system user for general operations.

---

## 2. Projects and Tools

- Application projects: `/opt/ontoportal`
    - **ontoportal_web_ui**: Frontend web interface.
    - **ontologies_api**: Backend API for ontology management.
    - **ncbo_cron**: Background cron jobs related to OntoPortal operations.
- Other tools (Databases, search engines): `/opt/ontoportal`
    - **virtuoso**: RDF triple store and SPARQL endpoint.
    - **solr**: Search indexing and retrieval.
    - **redis**: In-memory data structure store.

---

## 4. Sudo Commands for `ontoportal` User

The user `ontoportal` is allowed to execute the following commands with `sudo` without a password:

| **Command** | **Description** |
| --- | --- |
| `/usr/local/bin/oprestart` | Restart OntoPortal services |
| `/usr/local/bin/opstop` | Stop OntoPortal services |
| `/usr/local/bin/opstart` | Start OntoPortal services |
| `/usr/local/bin/opstatus` | Check the status of services |
| `/usr/local/bin/opclearcaches` | Clear all the caches |
| `systemctl start nginx` | Start Nginx |
| `systemctl stop nginx` | Stop Nginx |
| `systemctl restart nginx` | Restart Nginx |
| `systemctl start ncbo_cron` | Start NCBO cron jobs |
| `systemctl stop ncbo_cron` | Stop NCBO cron jobs |
| `systemctl restart ncbo_cron` | Restart NCBO cron jobs |
| `systemctl start solr` | Start Solr service |
| `systemctl stop solr` | Stop Solr service |
| `systemctl restart solr` | Restart Solr service |
| `systemctl start redis-server-*.service` | Start Redis server. |
| `systemctl stop redis-server-*.service` | Stop Redis server. |
| `systemctl restart redis-server-*.service` | Restart Redis server. |
| `/usr/sbin/virt-what` | Detect virtualization type. |
| `/opt/ontoportal/virtual_appliance/utils/bootstrap/gen_tlscert.sh` | Generate TLS certificate. |
| `/usr/sbin/service agraph start` | Start AllegroGraph. |
| `/usr/sbin/service agraph status` | Check AllegroGraph status. |
| `/usr/sbin/service agraph stop` | Stop AllegroGraph. |

---

## 5. Portal Configurations (TO-DO)

Configuration files for each project are located in their respective directories under `/opt/ontoportal/<project>/shared`. Key configuration files include:

- **ontoportal_web_ui:**
- **ontologies_api:**
- **ncbo_cron:**
- **virtuoso:**

---

## 6. Ontoportal-Astro license
- Private

---

## 7. Deploying the VM (TO-DO)

The VM is provided as an OVA file. Follow these steps to deploy it:

1. Download the OVA file.
2. Open VirtualBox or another virtualization tool.
3. Select **File > Import Appliance**.
4. Browse and select the OVA file.
5. Follow the import wizard and configure resources (CPU, RAM, Network, etc.). TO-DO
6. Start the VM and log in with the `ontoportal` user to manage the services.

---