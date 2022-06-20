# SH-HQ

Machine configuration and monitoring system.

## Help

hq

    Usage: hq [-v][op]
    
    List machines and define operation menus for them. The scripts
    are named MACHINE.sh and stored in ~/.hq or ${HQ_DIR}.
    
    Functions to define:
    
        - HQ_current()      : Returns success in the machine.
        - HQ_ssh([CMD])     : Executes a command in the machine.
        - HQ_menu()         : Opens a menu in the machine.
        - HQ_menu_local()   : Open a menu locally.
        - HQ_restart_cron() : Restart cron.
    
    You can also define periodic tasks with the following comments.
    
        #hcron[-local]: M H D M D F
        minute hour day-of-month month day-of-week function
    
        *     : 0  6 *   * *   : At 6:00 every day
        30    : 30 5 *   * 1-5 : At 5:30 every business day.
        */N   : 0  5 */3 * *   : At 5:00 every third day of month.
        1-5   : 
        1,3,6 : 
    
    Operations:
    
        ... show              : Show local configuration.
        ... ping              : Perform a ping on all machines.
        ... ssh-copy-all      : Copy SSH public keys to all machines.
        ... update-crontab    : Update the ~/.crontab-hq file.
        ... MACHINE [local]   : Execute the machine's menu remotelly.
        ... MACHINE exec FUNC : Execute a function remotelly.

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)

