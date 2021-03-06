# Rename-FileWithDateTakenExif

This PowerShell script reads the EXIF data of a file (if it exists) and prepends the `Date taken` field to the beginning of the file name.  The format is `MM-DD-YYYY-TTTT-[AM|PM]_<orig_filename>`

This script implements Ed Wilson's [Get-FileMetaDataReturnObject.ps1](https://gallery.technet.microsoft.com/scriptcenter/get-file-meta-data-function-f9e8d804) function.

## Example
This script should not reside in the same `path` as the data of interest.  Additionally, the `path` must be the directory of interest where the file(s) reside as the `COM Shell.Application` object operates on the directory and not the individual files.

```powershell
.\Rename-FileWithDateTakenExif.ps1 <directory_path>

# Example
.\Rename-FileWithDateTakenExif.ps1 c:\exif_pics\
```
