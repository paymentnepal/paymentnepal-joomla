# paymentnepal-joomla  
Plugins are designed for two different CMS versions:  
* joomla_25_3 for Joomla 2.5 and Joomla 3 
* joomla_15 for Joomla 1.5

Installation is similar

Installation guide:

1.  Enter your site administration panel, then go to Plugins -> Install/Uninstall

2.  In Upload menu click Browse and choose .zip file with plugin from your local computer, then click "Upload&Install"

3.  Go to the Materials -> Partition manager page

4.  Click "Create" button in the upper-right corner

5.  Fill in partition parameters. In "Deatils" group enter the name of new partition (for example "Payment") and click "Save"

6.  Go to "All menu" -> "Main menu" and click "Create"

7.  In "Choose menu type" group inside "Inner link" -> "Materials" -> "Partition" choose "Standard partition template"

8.  Set params for new menu:
    - in "Menu details" group enter name of menu (like "Payment");
    - in "Params" -> "Main" group choose name of the newly created partition from the "Partition" dropdown list. Click "Save"

9.  Go to "Plugins" -> "Plugin manager" and in the list of plugins installed click "paymentnepal payment gateway"

10. Set joomla_paymentnepal plugin settings:
    - inside "Details" group:
    -- set "Enabled" to "Yes";
    -- from "Position" dropdown list choose "Footer".
    - inside "menu purpose" group:
    -- select "Choose from list" option;
    -- from "Menu selection" dropdown list select a newly created menu.

11. Success/Fail/Result URL to fill in your Paymentnepal service settings can be obtained from "Plugin params" group

12. At the plugin params page set secret_key and payment_key inside "Plugin params" group and click "Save"

13. After that you'll see link to payment form on your site in the Main menu

14. Examples of callback handlers are presented in:
    - process.php allows to handle callback in case of successful payment
      (for example add a record about payment to database);
    - payed.php allows to inform customer about successful payment (for example give him access to content, link etc.);
    - fail.php allows to inform customer about failed payment attempt.
