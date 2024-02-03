# Monitoring_Docker_Ansible_

# Ansible Prometheus Grafana Monitoring Stack Installation
This Ansible repository provides code to install the Prometheus Grafana monitoring stack on different operating systems including CentOS, Debian, and Ubuntu. The installation process involves the following steps:

1. **Docker Installation**: Installs Docker on the target operating systems.

2. **Grafana and Prometheus Installation with Docker Compose**: Deploys Grafana and Prometheus using Docker Compose. The repository includes customizable Docker Compose templates (these templates are copies of good github repository which contains docker-compose deployment) that can be edited based on specific requirements. Ansible copies these Docker Compose files to servers grouped as per their monitoring requirements. For example, the repository includes groups such as [monitoring-servers] for hosts where Grafana and Prometheus are installed, as well as groups for specific services like Elasticsearch, RabbitMQ, Beats, Redis, uWSGI, and MySQL.

3. **Exporter Installation**: Installs exporters for different services on their respective hosts. The services and exporters are organized into specific groups recognized in the host file. Exporters for Elasticsearch, RabbitMQ, Beats, Redis, uWSGI, and MySQL are all installed using Docker Compose, and customizable Docker Compose files are provided in the template directory to allow users to tailor the configurations for their specific needs.

## Usage

To use this repository, follow these steps:

1. Update the hosts file with your server configurations and group them based on the services they provide. If encountering filtering limitations, you can define a proxy in the hosts file for the Ansible deployment.

2. Customize the Docker Compose files in the template directory according to your monitoring and exporting requirements.

3. Run the Ansible playbooks to install Docker, deploy Grafana and Prometheus, and install the exporters on your designated hosts.

## Contributing

Contributions are welcome! If you have any improvements or additional features to suggest, feel free to submit a pull request or open an issue to discuss your ideas.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


