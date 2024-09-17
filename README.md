# Automating Satisfactory Save Backup to GitHub

If anyone else wants to automate their Satisfactory save backups to GitHub, it's quite easy, and you can use my script and public GitHub repo.

## Steps

1. **Download the Script**:
   - Download the batch script and place it in `C:\scripts`.

2. **Download My Public GitHub Repo**:
   - Clone or download the public GitHub repository from [here](https://github.com/danieljrich/public-files/tree/main) and place the folder in `C:\git`.

3. **Update the Script**:
   - Open the script and update the top 3 environment variables:
     - `MY_NAME`: This will be the folder your file is saved to in the repo.
     - `SAVE_NAME`: The name of your save file.
     - `SAVE_PATH`: The path to your local Satisfactory save files.

4. **Set Up Windows Task Scheduler**:
   - Open **Windows Task Scheduler** and create a basic task:
     - **Trigger**: Set it to **Daily**.
     - **Action**: Browse to your script in `C:\scripts`.
     - **Finish** the basic task setup.
   
5. **Edit the Task in Task Scheduler**:
   - After creating the task, edit it:
     - **General Tab**: Select **Run whether user is logged on or not**.
     - **Triggers Tab**: Edit the trigger and, under **Advanced Settings**, configure the following:
       - **Repeat task every**: 5 minutes.
       - **For a duration of**: Indefinitely.

This setup will ensure your save file is backed up to GitHub every 5 minutes.
