---
UID: NS:shellapi._SHFILEOPSTRUCTA
title: SHFILEOPSTRUCTA (shellapi.h)
description: Contains information that the SHFileOperation function uses to perform file operations. (ANSI)
helpviewer_keywords: ["*LPSHFILEOPSTRUCTA","FOF_ALLOWUNDO","FOF_CONFIRMMOUSE","FOF_FILESONLY","FOF_MULTIDESTFILES","FOF_NOCONFIRMATION","FOF_NOCONFIRMMKDIR","FOF_NOCOPYSECURITYATTRIBS","FOF_NOERRORUI","FOF_NORECURSEREPARSE","FOF_NORECURSION","FOF_NO_CONNECTED_ELEMENTS","FOF_NO_UI","FOF_RENAMEONCOLLISION","FOF_SILENT","FOF_SIMPLEPROGRESS","FOF_WANTMAPPINGHANDLE","FOF_WANTNUKEWARNING","FO_COPY","FO_DELETE","FO_MOVE","FO_RENAME","LPSHFILEOPSTRUCT","LPSHFILEOPSTRUCT structure pointer [Windows Shell]","SHFILEOPSTRUCT","SHFILEOPSTRUCT structure [Windows Shell]","SHFILEOPSTRUCTA","_win32_SHFILEOPSTRUCT","shell.SHFILEOPSTRUCT","shellapi/LPSHFILEOPSTRUCT","shellapi/SHFILEOPSTRUCT"]
old-location: shell\SHFILEOPSTRUCT.htm
tech.root: shell
ms.assetid: 590d87c2-0c75-44b9-a9b5-f7c37728512b
ms.date: 12/05/2018
ms.keywords: '*LPSHFILEOPSTRUCTA, FOF_ALLOWUNDO, FOF_CONFIRMMOUSE, FOF_FILESONLY, FOF_MULTIDESTFILES, FOF_NOCONFIRMATION, FOF_NOCONFIRMMKDIR, FOF_NOCOPYSECURITYATTRIBS, FOF_NOERRORUI, FOF_NORECURSEREPARSE, FOF_NORECURSION, FOF_NO_CONNECTED_ELEMENTS, FOF_NO_UI, FOF_RENAMEONCOLLISION, FOF_SILENT, FOF_SIMPLEPROGRESS, FOF_WANTMAPPINGHANDLE, FOF_WANTNUKEWARNING, FO_COPY, FO_DELETE, FO_MOVE, FO_RENAME, LPSHFILEOPSTRUCT, LPSHFILEOPSTRUCT structure pointer [Windows Shell], SHFILEOPSTRUCT, SHFILEOPSTRUCT structure [Windows Shell], SHFILEOPSTRUCTA, _win32_SHFILEOPSTRUCT, shell.SHFILEOPSTRUCT, shellapi/LPSHFILEOPSTRUCT, shellapi/SHFILEOPSTRUCT'
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHFILEOPSTRUCTA, *LPSHFILEOPSTRUCTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHFILEOPSTRUCTA
 - shellapi/_SHFILEOPSTRUCTA
 - LPSHFILEOPSTRUCTA
 - shellapi/LPSHFILEOPSTRUCTA
 - SHFILEOPSTRUCTA
 - shellapi/SHFILEOPSTRUCTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - SHFILEOPSTRUCT - SHFILEOPSTRUCTA
---

# SHFILEOPSTRUCTA structure


## -description

Contains information that the <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function uses to perform file operations.

            
<div class="alert"><b>Note</b>  As of Windows Vista, the use of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> interface is recommended over this function.</div><div> </div>

## -struct-fields

### -field hwnd

Type: <b>HWND</b>

A window handle to the dialog box to display information about the status of the file operation.

### -field wFunc

Type: <b>UINT</b>

A value that indicates which operation to perform. One of the following values:



#### FO_COPY

Copy the files specified in the <b>pFrom</b> member to the location specified in the <b>pTo</b> member.



#### FO_DELETE

Delete the files specified in <b>pFrom</b>.



#### FO_MOVE

Move the files specified in <b>pFrom</b> to the location specified in <b>pTo</b>.



#### FO_RENAME

Rename the file specified in <b>pFrom</b>. You cannot use this flag to rename multiple files with a single function call. Use <b>FO_MOVE</b> instead.

### -field pFrom

Type: <b>PCZZTSTR</b>

<div class="alert"><b>Note</b>  This string must be double-null terminated.</div>
<div> </div>
A pointer to one or more source file names. These names should be fully qualified paths to prevent unexpected results.

Standard MS-DOS wildcard characters, such as "*", are permitted <i>only</i> in the file-name position. Using a wildcard character elsewhere in the string will lead to unpredictable results.

Although this member is declared as a single null-terminated string, it is actually a buffer that can hold multiple null-delimited file names. Each file name is terminated by a single <b>NULL</b> character. The last file name is terminated with a double <b>NULL</b> character ("\0\0") to indicate the end of the buffer.

### -field pTo

Type: <b>PCZZTSTR</b>

<div class="alert"><b>Note</b>  This string must be double-null terminated.</div>
<div> </div>
A pointer to the destination file or directory name. This parameter must be set to <b>NULL</b> if it is not used. Wildcard characters are not allowed. Their use will lead to unpredictable results.

Like <b>pFrom</b>, the <b>pTo</b> member is also a double-null terminated string and is handled in much the same way. However, <b>pTo</b> must meet the following specifications:

<ul>
<li>Wildcard characters are not supported.</li>
<li>Copy and Move operations can specify destination directories that do not exist. In those cases, the system attempts to create them and normally displays a dialog box to ask the user if they want to create the new directory. To suppress this dialog box and have the directories created silently, set the <b>FOF_NOCONFIRMMKDIR</b> flag in <b>fFlags</b>.</li>
<li>For Copy and Move operations, the buffer can contain multiple destination file names if the <b>fFlags</b> member specifies <b>FOF_MULTIDESTFILES</b>.</li>
<li>Pack multiple names into the <b>pTo</b> string in the same way as for <b>pFrom</b>.</li>
<li>Use fully qualified paths. Using relative paths is not prohibited, but can have unpredictable results.</li>
</ul>

### -field fFlags

Type: <b>FILEOP_FLAGS</b>

Flags that control the file operation. This member can take a combination of the following flags.



#### FOF_ALLOWUNDO

Preserve undo information, if possible. 
                        
                            

Prior to Windows Vista, operations could be undone only from the same process that performed the original operation.

In Windows Vista and later systems, the scope of the undo is a user session. Any process running in the user session can undo another operation. The undo state is held in the Explorer.exe process, and as long as that process is running, it can coordinate the undo functions.

If the source file parameter does not contain fully qualified path and file names, this flag is ignored.



#### FOF_CONFIRMMOUSE

Not used.



#### FOF_FILESONLY

Perform the operation only on files (not on folders) if a wildcard file name (*.*) is specified.



#### FOF_MULTIDESTFILES

The <b>pTo</b> member specifies multiple destination files (one for each source file in <b>pFrom</b>) rather than one directory where all source files are to be deposited.



#### FOF_NOCONFIRMATION

Respond with <b>Yes to All</b> for any dialog box that is displayed.



#### FOF_NOCONFIRMMKDIR

Do not ask the user to confirm the creation of a new directory if the operation requires one to be created.



#### FOF_NO_CONNECTED_ELEMENTS


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0.</a> Do not move connected files as a group. Only move the specified files.



#### FOF_NOCOPYSECURITYATTRIBS


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 4.71.</a> Do not copy the security attributes of the file. The destination file receives the security attributes of its new folder.



#### FOF_NOERRORUI

Do not display a dialog to the user if an error occurs.



#### FOF_NORECURSEREPARSE

Not used.



#### FOF_NORECURSION

Only perform the operation in the local directory. Do not operate recursively into subdirectories, which is the default behavior.



#### FOF_NO_UI


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Windows Vista</a>. Perform the operation silently, presenting no UI to the user. This is equivalent to FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOERRORUI | FOF_NOCONFIRMMKDIR.



#### FOF_RENAMEONCOLLISION

Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists at the destination.



#### FOF_SILENT

Do not display a progress dialog box.



#### FOF_SIMPLEPROGRESS

Display a progress dialog box but do not show individual file names as they are operated on.



#### FOF_WANTMAPPINGHANDLE

If <b>FOF_RENAMEONCOLLISION</b> is specified and any files were renamed, assign a name mapping object that contains their old and new names to the <b>hNameMappings</b> member. This object must be freed using <a href="/windows/desktop/api/shellapi/nf-shellapi-shfreenamemappings">SHFreeNameMappings</a> when it is no longer needed.



#### FOF_WANTNUKEWARNING


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0.</a> Send a warning if a file is being permanently destroyed during a delete operation rather than recycled. This flag partially overrides <b>FOF_NOCONFIRMATION</b>.

### -field fAnyOperationsAborted

Type: <b>BOOL</b>

When the function returns, this member contains <b>TRUE</b> if any file operations were aborted before they were completed; otherwise, <b>FALSE</b>. An operation can be manually aborted by the user through UI or it can be silently aborted by the system if the FOF_NOERRORUI or FOF_NOCONFIRMATION flags were set.

### -field hNameMappings

Type: <b>LPVOID</b>

When the function returns, this member contains a handle to a name mapping object that contains the old and new names of the renamed files. This member is used only if the <b>fFlags</b> member includes the <b>FOF_WANTMAPPINGHANDLE</b> flag. See Remarks for more details.

### -field lpszProgressTitle

Type: <b>PCTSTR</b>

A pointer to the title of a progress dialog box. This is a null-terminated string. This member is used only if <b>fFlags</b> includes the <b>FOF_SIMPLEPROGRESS</b> flag.

## -remarks

<div class="alert"><b>Important</b>  You must ensure that the source and destination paths are double-null terminated. A normal string ends in just a single null character. If you pass that value in either the source or destination members, the function will not realize when it has reached the end of the string and will continue to read on in memory until it comes to a random double null value. This can at least lead to a buffer overrun, and possibly the unintended deletion of unrelated data.

</div>
<div> </div>

```cpp
// WRONG
LPTSTR pszSource = L"C:\\Windows\\*";

// RIGHT
LPTSTR pszSource = L"C:\\Windows\\*\0";

```


To account for the two terminating null characters, be sure to create buffers large enough to hold MAX_PATH (which normally includes the single terminating null character) plus 1.

It cannot be overstated that your paths should always be full paths. If the <b>pFrom</b> or <b>pTo</b> members are unqualified names, the current directories are taken from the global current drive and directory settings as managed by the <a href="/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a> and <a href="/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory">SetCurrentDirectory</a> functions.

                

If you do not provide a full path, the following facts become pertinent:
                
<ul>
<li>The lack of a path before a file name does not indicate to <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> that this file resides in the root of the current directory.</li>
<li>The PATH environment variable is not used by <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> to determine a valid path.</li>
<li>
<a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> cannot be relied on to use the directory that is the current directory when it begins executing. The directory seen as the current directory is process-wide, and it can be changed from another thread while the operation is executing. If that were to happen, the results of <b>SHFileOperation</b> would be unpredictable.</li>
</ul>


If <b>pFrom</b> is set to a file name without a full path, deleting the file with <b>FO_DELETE</b> does not move it to the Recycle Bin, even if the <b>FOF_ALLOWUNDO</b> flag is set. You must provide a full path to delete the file to the Recycle Bin.


<a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> fails on any path prefixed with "\\?\".

There are two versions of this structure, an ANSI version (SHFILEOPSTRUCTA) and a Unicode version (SHFILEOPSTRUCTW). The Unicode version is identical to the ANSI version, except that wide character strings (<b>LPCWSTR</b>) are used in place of ANSI character strings (<b>LPCSTR</b>). On Windows 98 and earlier, only the ANSI version is supported. On Microsoft Windows NT 4.0 and later, both the ANSI and Unicode versions of this structure are supported. SHFILEOPSTRUCTW and SHFILEOPTSTRUCTA should never be used directly; the appropriate structure is redefined as <b>SHFILEOPSTRUCT</b> by the precompiler depending on whether the application is compiled for ANSI or Unicode. 

                


<a href="/windows/desktop/api/shellapi/ns-shellapi-shnamemappinga">SHNAMEMAPPING</a> has similar ANSI and Unicode versions. For ANSI applications, <b>hNameMappings</b> points to an <b>int</b> followed by an array of ANSI <b>SHNAMEMAPPING</b> structures. For Unicode applications, <b>hNameMappings</b> points to an <b>int</b> followed by an array of Unicode <b>SHNAMEMAPPING</b> structures. However, on Microsoft Windows NT 4.0 and later, <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> <i>always</i> returns a handle to a Unicode set of <b>SHNAMEMAPPING</b> structures. If you want applications to be functional with all versions of Windows, the application must employ conditional code to deal with name mappings. For example:


```cpp
x = SHFileOperation(&shop);

if (fWin9x) 
    HandleAnsiNameMappings(shop.hNameMappings);
else 
    HandleUnicodeNameMappings(shop.hNameMappings);

```


Treat <b>hNameMappings</b> as a pointer to a structure whose members are a <b>UINT</b> value followed by a pointer to an array of <a href="/windows/desktop/api/shellapi/ns-shellapi-shnamemappinga">SHNAMEMAPPING</a> structures, as seen in its declaration:

				


```cpp
struct HANDLETOMAPPINGS 
{
    UINT              uNumberOfMappings;  // Number of mappings in the array.
    LPSHNAMEMAPPING   lpSHNameMapping;    // Pointer to the array of mappings.
};

```


The <b>UINT</b> value indicates the number of <a href="/windows/desktop/api/shellapi/ns-shellapi-shnamemappinga">SHNAMEMAPPING</a> structures in the array. Each <b>SHNAMEMAPPING</b> structure contains the old and new path for one of the renamed files.

<div class="alert"><b>Note</b>  The handle must be freed with <a href="/windows/desktop/api/shellapi/nf-shellapi-shfreenamemappings">SHFreeNameMappings</a>.</div>
<div> </div>



> [!NOTE]
> The shellapi.h header defines SHFILEOPSTRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
