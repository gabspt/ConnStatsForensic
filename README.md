# ConnStatsForensic
Repository created for testing ConnStats Probe with Tcpreplay captures. Valid for scenarios where observed traffic is only ingress.

Forensic mode aggregates packets into flows and generates post-mortem statistics when the capture has finised and the program is manually stopped.

# Requirements
Inside Requirements folder can be found the installed libraries and dependencies to run the programs in Ubuntu 22.04.3 LTS

To reinstall them in your system use the following comands:

dpkg --get-selections < ubuntu_installed_packages.txt
apt-get dselect-upgrade

pip install -r requirements_python.txt

with the go.mod and go.sum files copied in the environments run:
go mod download


# Run the programs
To run one of the ConnStats mode programs, go to cmd folder.

cd cmd
sudo go run connstats.go [options]

current options are:

-i <interface> : network interface to attach the ebpf program, by default is enp0s8




