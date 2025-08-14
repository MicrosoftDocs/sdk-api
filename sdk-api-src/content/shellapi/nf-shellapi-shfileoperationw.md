---
UID: NF:shellapi.SHFileOperationW
title: SHFileOperationW function (shellapi.h)
description: Copies, moves, renames, or deletes a file system object. On Windows Vista and later releases, we recommend that you use IFileOperation instead of this function.
helpviewer_keywords: ["SHFileOperation", "SHFileOperation function [Windows Shell]", "SHFileOperationW", "_win32_SHFileOperation", "shell.SHFileOperation", "shellapi/SHFileOperation", "shellapi/SHFileOperationW"]
old-location: shell\SHFileOperation.htm
tech.root: shell
ms.assetid: 7807015f-52c5-46f5-9e90-4e3e60ddf705
ms.date: 12/05/2018
ms.keywords: SHFileOperation, SHFileOperation function [Windows Shell], SHFileOperationA, SHFileOperationW, _win32_SHFileOperation, shell.SHFileOperation, shellapi/SHFileOperation, shellapi/SHFileOperationA, shellapi/SHFileOperationW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHFileOperationW (Unicode) and SHFileOperationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHFileOperationW
 - shellapi/SHFileOperationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHFileOperation
 - SHFileOperationA
 - SHFileOperationW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHFileOperationW function


## -description

Copies, moves, renames, or deletes a file system object. This function has been replaced in Windows Vista by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>.

## -parameters

### -param lpFileOp [in, out]

Type: <b>LPSHFILEOPSTRUCT</b>

A pointer to an <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa">SHFILEOPSTRUCT</a> structure that contains information this function needs to carry out the specified operation. This parameter must contain a valid value that is not <b>NULL</b>. You are responsible for validating the value. If you do not validate it, you will experience unexpected results.

## -returns

Type: <b>int</b>

Returns zero if successful; otherwise nonzero. Applications normally should simply check for zero or nonzero. 

                    

It is good practice to examine the value of the <b>fAnyOperationsAborted</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa">SHFILEOPSTRUCT</a>. <b>SHFileOperation</b> can return 0 for success if the user cancels the operation. If you do not check <b>fAnyOperationsAborted</b> as well as the return value, you cannot know that the function accomplished the full task you asked of it and you might proceed under incorrect assumptions.

Do not use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> with the return values of this function.

To examine the nonzero values for troubleshooting purposes, they largely map to those defined in Winerror.h. However, several of its possible return values are based on pre-Win32 error codes, which in some cases overlap the later Winerror.h values without matching their meaning. Those particular values are detailed here, and <i>for these specific values only</i> these meanings should be accepted over the Winerror.h codes. However, these values are provided with these warnings:

<ul>
<li>These are pre-Win32 error codes and are no longer supported or defined in any public header file. To use them, you must either define them yourself or compare against the numerical value.</li>
<li>These error codes are subject to change and have historically done so.</li>
<li>These values are provided only as an aid in debugging. They should not be regarded as definitive.</li>
</ul>


<table class="clsStd">
<tr>
<th>Error Code</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DE_SAMEFILE</td>
<td>0x71</td>
<td>The source and destination files are the same file.</td>
</tr>
<tr>
<td>DE_MANYSRC1DEST</td>
<td>0x72</td>
<td>Multiple file paths were specified in the source buffer, but only one destination file path.</td>
</tr>
<tr>
<td>DE_DIFFDIR</td>
<td>0x73</td>
<td>Rename operation was specified but the destination path is a different directory. Use the move operation instead.</td>
</tr>
<tr>
<td>DE_ROOTDIR</td>
<td>0x74</td>
<td>The source is a root directory, which cannot be moved or renamed.</td>
</tr>
<tr>
<td>DE_OPCANCELLED</td>
<td>0x75</td>
<td>The operation was canceled by the user, or silently canceled if the appropriate flags were supplied to <b>SHFileOperation</b>.</td>
</tr>
<tr>
<td>DE_DESTSUBTREE</td>
<td>0x76</td>
<td>The destination is a subtree of the source.</td>
</tr>
<tr>
<td>DE_ACCESSDENIEDSRC</td>
<td>0x78</td>
<td>Security settings denied access to the source.</td>
</tr>
<tr>
<td>DE_PATHTOODEEP</td>
<td>0x79</td>
<td>The source or destination path exceeded or would exceed MAX_PATH.</td>
</tr>
<tr>
<td>DE_MANYDEST</td>
<td>0x7A</td>
<td>The operation involved multiple destination paths, which can fail in the case of a move operation.</td>
</tr>
<tr>
<td>DE_INVALIDFILES</td>
<td>0x7C</td>
<td>The path in the source or destination or both was invalid.</td>
</tr>
<tr>
<td>DE_DESTSAMETREE</td>
<td>0x7D</td>
<td>The source and destination have the same parent folder.</td>
</tr>
<tr>
<td>DE_FLDDESTISFILE</td>
<td>0x7E</td>
<td>The destination path is an existing file.</td>
</tr>
<tr>
<td>DE_FILEDESTISFLD</td>
<td>0x80</td>
<td>The destination path is an existing folder.</td>
</tr>
<tr>
<td>DE_FILENAMETOOLONG</td>
<td>0x81</td>
<td>The name of the file exceeds MAX_PATH.</td>
</tr>
<tr>
<td>DE_DEST_IS_CDROM</td>
<td>0x82</td>
<td>The destination is a read-only CD-ROM, possibly unformatted.</td>
</tr>
<tr>
<td>DE_DEST_IS_DVD</td>
<td>0x83</td>
<td>The destination is a read-only DVD, possibly unformatted.</td>
</tr>
<tr>
<td>DE_DEST_IS_CDRECORD</td>
<td>0x84</td>
<td>The destination is a writable CD-ROM, possibly unformatted.</td>
</tr>
<tr>
<td>DE_FILE_TOO_LARGE</td>
<td>0x85</td>
<td>The file involved in the operation is too large for the destination media or file system.</td>
</tr>
<tr>
<td>DE_SRC_IS_CDROM</td>
<td>0x86</td>
<td>The source is a read-only CD-ROM, possibly unformatted.</td>
</tr>
<tr>
<td>DE_SRC_IS_DVD</td>
<td>0x87</td>
<td>The source is a read-only DVD, possibly unformatted.</td>
</tr>
<tr>
<td>DE_SRC_IS_CDRECORD</td>
<td>0x88</td>
<td>The source is a writable CD-ROM, possibly unformatted.</td>
</tr>
<tr>
<td>DE_ERROR_MAX</td>
<td>0xB7</td>
<td>MAX_PATH was exceeded during the operation.</td>
</tr>
<tr>
<td></td>
<td>0x402</td>
<td>An unknown error occurred. This is typically due to an invalid path in the source or destination. This error does not occur on Windows Vista and later.</td>
</tr>
<tr>
<td>ERRORONDEST</td>
<td>0x10000</td>
<td>An unspecified error occurred on the destination.</td>
</tr>
<tr>
<td>DE_ROOTDIR | ERRORONDEST</td>
<td>0x10074</td>
<td>Destination is a root directory and cannot be renamed.</td>
</tr>
</table>

## -remarks

You should use fully qualified path names with this function. Using it with relative path names is not thread safe.

With two exceptions, you cannot use <b>SHFileOperation</b> to move special folders from a local drive to a remote computer by specifying a network path. The exceptions are the <b>My Documents</b> (<a href="/windows/desktop/shell/csidl">CSIDL_PERSONAL</a>, <a href="/windows/desktop/shell/csidl">CSIDL_DOCUMENTS</a>) and <b>My Pictures</b> folders (<a href="/windows/desktop/shell/csidl">CSIDL_MYPICTURES</a>).

When used to delete a file, <b>SHFileOperation</b> permanently deletes the file unless you set the <b>FOF_ALLOWUNDO</b> flag in the <b>fFlags</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa">SHFILEOPSTRUCT</a> structure pointed to by <i>lpFileOp</i>. Setting that flag sends the file to the Recycle Bin. If you want to simply delete a file and guarantee that it is not placed in the Recycle Bin, use <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>.

If a copy callback handler is exposed and registered, <b>SHFileOperation</b> calls it unless you set a flag such as <b>FOF_NOCONFIRMATION</b> in the <b>fFlags</b> member of the structure pointed to by <i>lpFileOp</i>. See <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)">ICopyHook::CopyCallback</a> for details on implementing copy callback handlers.

File deletion is recursive unless you set the <b>FOF_NORECURSION</b> flag in <i>lpFileOp</i>.

<h3><a id="Connecting_Files"></a><a id="connecting_files"></a><a id="CONNECTING_FILES"></a>Connecting Files</h3>
With Windows 2000 or later, it is possible to <i>connect</i> an HTML file with a folder that contains related files such as Graphics Interchange Format (GIF) images or style sheets. If file connection is enabled, when you move or copy the HTML file, the connected folder and all of its files are also moved or copied. Conversely, if you move the folder with the related files, the HTML file is also moved.

The HTML file must have a .htm or .html extension. You create the connection to the related files by placing the folder that contains them into the same folder as the HTML file. The name of the folder that contains the connected files must be the same as the name of the HTML file followed by "_files" or ".files" (this is case sensitive; for example, ".Files" does not work). An example is given here.

<ol>
<li>Create a file named Test.htm in the C:\Files directory (C:\Files\Test.htm).</li>
<li>Create a new folder named Test.files in the C:\Files directory (C:\Files\Test.files).</li>
<li>Populate the folder with a few files. Any file placed in this folder is connected to Test.htm.</li>
<li>Move or copy the Test.htm file to the C:\Files2 directory.</li>
<li>Note that the Test.files directory is now found in the C:\Files2 directory as well.</li>
</ol>


File connection is enabled by default. It can be disabled by adding a <b>REG_DWORD</b> entry, NoFileFolderConnection, as shown here:


<pre><b>HKEY_CURRENT_USER</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>NoFileFolderConnection</b></pre>


Setting NoFileFolderConnection to 1 disables file connection. If the value is set to zero or is missing, file connection is enabled.

To move only the specified files and none of the connected files, set the <b>FOF_NO_CONNECTED_ELEMENTS</b> flag in the <b>fFlags</b> member of the structure pointed to by <i>lpFileOp</i>.

Note that the use of a folder with a name like "MyFile_files" to define a connection may not be valid for localized versions of Windows. The term "files" may need to be replaced by the equivalent word in the local language.




> [!NOTE]
> The shellapi.h header defines SHFileOperation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
