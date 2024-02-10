# Proxmox Autosnap in bash

## Usage
```bash
# Example: Take a new snapshot of all VMs except 108 and 109,
# label it "hourly", keep only 12 snaps with this label
proxmox-autosnap.bsh --create --destroy --vmid all --type hourly --exclude 108,109 --keep 12

  -c --create:
      Create snapshots

  -d --destroy
    Destroy snapshots, use with --keep

  -l --list
    List snapshots

  -v --vmid
    Comma-separated list of VMIDs, or "all"

  -r --running
    Limit snapshots to VMs that are currently running

  -t --type
    Snapshot type: hourly, daily, weekly, monthly, yearly

  -k --keep
    Number of snapshots to keep

  -e --exclude
    Comma-separated list of VMIDs to exclude, use with "--vmid all" to make exceptions
