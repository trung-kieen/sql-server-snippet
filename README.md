# Setup
Put these snippet file in to folder store snippet
- Clone repo
- Go to Document 
- `\Documents\SQL Server Management Studio\Code Snippets\SQL\My Code Snippets\` Naviagate your directory like this 
- Put all file extension .snippet into this folder

Or you just open powershell and run these command ^^ (require git and properly version of powershell)
```ps1
$documentPath = "$env:USERPROFILE\Documents\SQL Server Management Studio\Code Snippets\SQL\My Code Snippets\"
$destinationFolder = $documentPath

git clone https://github.com/trung-kieen/sql-server-snippet
Get-ChildItem -Path "sql-server-snippet" -Filter *.snippet | ForEach-Object {
    Move-Item -Path $_.FullName -Destination $destinationFolder -Force
}

```
# Usage
- Open ssms
- Connect server 
- Open new script file 
- Active hotkey Ctrl+K, Ctrl+X (press Ctrl K => release => press Ctrl X)
- Choose or type `My Code Snippets` 
- Choose whatever you want, you're all set 