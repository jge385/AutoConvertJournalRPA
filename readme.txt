Config.xlsx
	Before running, populate the value fields of attachmentsPath, outputFolderLocation and outlookAppLocation 
	if this is different on your machine. 

	- attachmentsPath: specifies the folder location where attachment csv journals will be downloaded during runtime
	- outputFolderLocation: specifies the location where the output formatted journals will be saved
	- journalEmailSubject: specifies term used to search for transaction journal emails by subject

	Please ensure this config file is closed before running the solution

Email Input
	In order to use the application you must have either an IMAP enabled gmail account (student university emails
	do not work), or a desktop outlook calendar application on which you are logged into. During runtime you will 
	be able to select which email system you are using. 

	This account used must have have an email in its inbox with subject corresponding exactly to that which is contained in 
	the value for journalEmailSubject in the config (TransactionsJournal by default). This email should contain the provided
	CSV journal ('Original Report.csv') as an attachment.
	
	If you are using an IMAP enabled gmail account, you will be prompted to enter your email and password. For gmail
	accounts this must be an 'App Password', as documented here: https://support.google.com/accounts/answer/185833?hl=en
	If you attempt to login with your regular gmail password it will fail.

Execution
	In order to execute the application, unzip the project contents to a suitable location. Then, open UiPath Studio
	and open the project.json file. Once you have populated the config file, and have an email containing the attachment
	CSV journal (with subject corresponding to that in your config), execute the workflow by running Main.xaml. You will
	be prompted to select either an Outlook or IMAP based execution, so select the one which you have setup with the 
	test input email. Once the process completes your converted journal, and a list of any erroneous rows will be 
	saved to the folder which you specified in the Config.xlsx.
	