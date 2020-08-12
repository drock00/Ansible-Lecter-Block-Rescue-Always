
# Ansible-Lecter-Block-Rescue-Always

### Using Block, Rescue, Always to Perform Groups of Tasks Based on Sucess or Failure  

This play is similar to what Sander van Vugt propses in his lecture about attempting to remove the meminfo file which cannot be done. Here, in the block, I attempt to do the same which will fail. Thus, rescue picks up its task which is to copy an IMPORTANT file over to the /tmp directory. Lastly, the play will always check the hostname.

# Example Run 1
```sh
$ ansible-playbook block_rescue.yml 
```

# Validate using adhoc

```sh
$ ansible-playbook ansible24.example.com -m shell -a "ls /tmp"
```

### Tech and Running the file

You need a control and managed node to test the block/rescue/always. Use an adhoc command to check for the IMPORTANT file in /tmp to verify rescue worked. Alternatively, edit the block to try to remove a file that's possible to remove.