**Repository Name: 3X-UI + Traefik Server Configuration**

**Description:**
This repository contains the Docker Compose configuration for setting up 3x-ui server. With Docker containers, it enables easy deployment and management.
The setup includes a combination of tools and services aimed at enhancing internet privacy.

**Included Services:**

**3X-UI**: An Advanced Web Panel • Built on Xray Core

**Traefik**: A reverse proxy and load balancer, managing traffic and enabling secure access to the various services deployed on the server.

**Usage:**

1. **Prerequisites**:
   - Docker and Docker Compose installed on the host server.
   - Ensure ports required by individual services are available and not conflicting with existing services on the server.

2. **Clone the Repository**:
   ```bash
   git clone https://github.com/gentslava/3x-ui_traefik.git
   cd 3x-ui_traefik
   ```

3. **Configuration**:
   - Create `.env` and other files for properly work.
     ```bash
     bash init.sh
     ```
   - Customize the `.env` file with your preferred environment variables such as domain, subdomain postfix (differnt countries code for example), email for acme challenge. Use `.env.dist` for template.
   - Modify the `docker-compose.yml` file if necessary to adjust volumes, ports, or other configurations.

4. **Deploy Services**:
   ```bash
   docker compose up -d
   ```

5. **Accessing Services**:
   - Once the containers are up and running, access each service through your web browser.
   - Traefik manages access to services based on defined rules and paths. Refer to Traefik documentation for configuring additional routes and settings.

6. **Updating Services**:
   - Pull the latest changes from this repository.
   - Recreate containers to apply changes:
     ```bash
     docker compose down
     docker compose pull
     docker compose up -d
     ```

**License:**
This repository is provided under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and distribute the code as per the terms of the license.
