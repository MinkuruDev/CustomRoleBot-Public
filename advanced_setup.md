# Advanced setup with Custom Role Bot

*To use advanced setup, you have to understand everything that explained in **Basic Setup** (`/help option:setup`)*

In **Step 1** of **Basic Setup** drag role **@Custom Role Bot** high help to ensure bot always have higher role and able to mange custom role, you don't need to drag role **@Custom Role Bot** high BUT the bot require to have at least one role that higher than ALL custom role in the server.

In **Step 2** of **Basic Setup**, you don't need to drag exist custom role behind **@Custom Role Bot**, but now you have to choose a **@\<Start Role>** that right behind **@\<Start Role>** is the list of exist custom role (**@\<Start Role>** is not count as custom role).
If you drag **@Custom Role Bot** above your list of exist custom role, It's dose 2 things: Make bot able to manage custom role and also act as the **@\<Start Role>**

In **Step 3** of **Basic Setup** You don't have to create **@End Custom Role** but like **@\<Start Role>**, you need to choose a **@\<End Role>** that right above **@\<End Role>** is the list of exist custom role (**@\<End Role>** is not count as custom role).

In **Step 4** of **Basic Setup** We setup with:
`/setup start_role:@Custom Role Bot stop_role:@End Custom Role`
But now in **Advanced Setup**, replace `start_role` with **@\<Start Role>** selected above and `end_role` with **@\<End Role>**

In **Step 5** of **Basic Setup**, We go to ***[Server Settings > Intergration > Custom Role Bot]*** to modify what role can use `/cr_create` command.
By default, everyone can use `/cr_edit` command (they can't create new but can edit existing. EX: server booster after lost the booster role can still edit their role that created earlier). You can modify `/cr_edit` command sync with `/cr_create`.

## Example for Advanced setup
If a server role list look like this:
@Administrator
@Moderator
@BOT
@\<custom role 1>
@\<custom role 2>
...
@\<custom role n>
@Server Booster
@Level 100
@level 90
...
@Custom Role Bot
@\<everyone>

The **@\<Start Role>** in this situation is **@BOT** and the **@\<End Role>** is **@Server Booster** (Assume that Custom Role Bot has **@BOT** role)
The `/setup` for this example is:
`/setup start_role:@BOT stop_role:@Server Booster`

