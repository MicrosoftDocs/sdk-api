---
UID: NF:winbase.OpenFile
title: OpenFile function (winbase.h)
description: Creates, opens, reopens, or deletes a file.
helpviewer_keywords: ["OF_CANCEL","OF_CREATE","OF_DELETE","OF_EXIST","OF_PARSE","OF_PROMPT","OF_READ","OF_READWRITE","OF_REOPEN","OF_SHARE_COMPAT","OF_SHARE_DENY_NONE","OF_SHARE_DENY_READ","OF_SHARE_DENY_WRITE","OF_SHARE_EXCLUSIVE","OF_VERIFY","OF_WRITE","OpenFile","OpenFile function [Files]","_win32_openfile","base.openfile","fs.openfile","winbase/OpenFile"]
old-location: fs\openfile.htm
tech.root: fs
ms.assetid: 800f4d40-252a-44fe-b10d-348c22d69355
ms.date: 12/05/2018
ms.keywords: OF_CANCEL, OF_CREATE, OF_DELETE, OF_EXIST, OF_PARSE, OF_PROMPT, OF_READ, OF_READWRITE, OF_REOPEN, OF_SHARE_COMPAT, OF_SHARE_DENY_NONE, OF_SHARE_DENY_READ, OF_SHARE_DENY_WRITE, OF_SHARE_EXCLUSIVE, OF_VERIFY, OF_WRITE, OpenFile, OpenFile function [Files], _win32_openfile, base.openfile, fs.openfile, winbase/OpenFile
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenFile
 - winbase/OpenFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - OpenFile
---

# OpenFile function


## -description

Creates, opens, reopens, or deletes a file.
<div class="alert"><b>Note</b>  This function has limited capabilities and is not recommended. For new application development, use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.</div><div> </div>

## -parameters

### -param lpFileName [in]

The name of the file.

The string must consist of characters from the 8-bit Windows character set. The 
       <b>OpenFile</b> function does not support Unicode file names or 
       opening named pipes.

### -param lpReOpenBuff [out]

A pointer to the <a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a> structure that receives 
       information about a file when it is first opened.

The structure can be used in subsequent calls to the 
       <b>OpenFile</b> function to see an open file.

The <a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a> structure contains a path string 
       member with a length that is limited to <b>OFS_MAXPATHNAME</b> characters, which is 128 
       characters. Because of this, you cannot use the <b>OpenFile</b> 
       function to open a file with a path length that exceeds 128 characters. The 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function does not have this path 
       length limitation.

### -param uStyle [in]

The action to be taken.

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OF_CANCEL"></a><a id="of_cancel"></a><dl>
<dt><b>OF_CANCEL</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Ignored.

To produce a dialog box containing a <b>Cancel</b> button, use 
         <b>OF_PROMPT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_CREATE"></a><a id="of_create"></a><dl>
<dt><b>OF_CREATE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Creates a new file.

If the file exists, it is truncated to zero (0) length.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_DELETE"></a><a id="of_delete"></a><dl>
<dt><b>OF_DELETE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Deletes a file.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_EXIST"></a><a id="of_exist"></a><dl>
<dt><b>OF_EXIST</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Opens a file and then closes it.

Use this to test for the existence of a file.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_PARSE"></a><a id="of_parse"></a><dl>
<dt><b>OF_PARSE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Fills the <a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a> structure, but does not do 
         anything else.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_PROMPT"></a><a id="of_prompt"></a><dl>
<dt><b>OF_PROMPT</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Displays a dialog box if a requested file does not exist.

A dialog box informs a user that the system cannot find a file, and it contains 
         <b>Retry</b> and <b>Cancel</b> buttons. The 
         <b>Cancel</b> button directs <b>OpenFile</b> 
         to return a file-not-found error message.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_READ"></a><a id="of_read"></a><dl>
<dt><b>OF_READ</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Opens a file for reading only.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_READWRITE"></a><a id="of_readwrite"></a><dl>
<dt><b>OF_READWRITE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Opens a file with read/write permissions.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_REOPEN"></a><a id="of_reopen"></a><dl>
<dt><b>OF_REOPEN</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Opens a file by using information in the reopen buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_COMPAT"></a><a id="of_share_compat"></a><dl>
<dt><b>OF_SHARE_COMPAT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
For MS-DOS–based file systems, opens a file with compatibility mode, allows any 
         process on a specified computer to open the file any number of times.

Other efforts to open a file with other sharing modes fail. This flag is mapped to the 
         <b>FILE_SHARE_READ</b>|<b>FILE_SHARE_WRITE</b> flags of the 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_DENY_NONE"></a><a id="of_share_deny_none"></a><dl>
<dt><b>OF_SHARE_DENY_NONE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Opens a file without denying read or write access to other processes.

On MS-DOS-based file systems, if the file has been opened in compatibility mode by any other process, the 
         function fails.

This flag is mapped to the 
         <b>FILE_SHARE_READ</b>|<b>FILE_SHARE_WRITE</b> flags of the 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_DENY_READ"></a><a id="of_share_deny_read"></a><dl>
<dt><b>OF_SHARE_DENY_READ</b></dt>
<dt>0x00000030</dt>
</dl>
</td>
<td width="60%">
Opens a file and denies read access to other processes.

On MS-DOS-based file systems, if the file has been opened in compatibility mode, or for read access by any 
         other process, the function fails.

This flag is mapped to the <b>FILE_SHARE_WRITE</b> flag of the 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_DENY_WRITE"></a><a id="of_share_deny_write"></a><dl>
<dt><b>OF_SHARE_DENY_WRITE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Opens a file and denies write access to other processes.

On MS-DOS-based file systems, if a file has been opened in compatibility mode, or for write access by any 
         other process, the function fails.

This flag is mapped to the <b>FILE_SHARE_READ</b> flag of the 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_SHARE_EXCLUSIVE"></a><a id="of_share_exclusive"></a><dl>
<dt><b>OF_SHARE_EXCLUSIVE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Opens a file with exclusive mode, and denies both read/write access to other processes. If a file has been 
         opened in any other mode for read/write access, even by the current process, the function fails.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_VERIFY"></a><a id="of_verify"></a><dl>
<dt><b>OF_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Verifies that the date and time of a file are the same as when it was opened previously.

This is useful as an extra check for read-only files.

</td>
</tr>
<tr>
<td width="40%"><a id="OF_WRITE"></a><a id="of_write"></a><dl>
<dt><b>OF_WRITE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Opens a file for write access only.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value specifies a file handle to use when performing file I/O. To close the file, call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function using this handle.

If the function fails, the return value is <b>HFILE_ERROR</b>. To get extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>lpFileName</i> parameter specifies a file name and extension only, this function 
    searches for a matching file in the following directories and the order shown:

<ol>
<li>
The directory where an application is loaded.

</li>
<li>
The current directory.

</li>
<li>
The Windows system directory.

Use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a> function to get the 
       path of this directory.

</li>
<li>
The 16-bit Windows system directory.

There is not a function that retrieves the path of this directory, but it is searched.

</li>
<li>
The Windows directory.

Use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a> function to get 
       the path of this directory.

</li>
<li>
The directories that are listed in the PATH environment variable.

</li>
</ol>
The <i>lpFileName</i> parameter cannot contain wildcard characters.

The <b>OpenFile</b> function does not support the 
    <b>OF_SEARCH</b> flag that the 16-bit Windows 
    <b>OpenFile</b> function supports. The 
    <b>OF_SEARCH</b> flag directs the system to search for a matching file even when a file name 
    includes a full path. Use the <a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> function to search 
    for a file.

A sharing violation occurs if an attempt is made to open a file or directory for deletion on a remote machine 
    when the value of the <i>uStyle</i> parameter is the <b>OF_DELETE</b> access 
    flag OR'ed with any other access flag, and the remote file or directory has not been opened with 
    <b>FILE_SHARE_DELETE</b> share access. To avoid the sharing violation in this scenario, open 
    the remote file or directory with <b>OF_DELETE</b> access only, or call 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a> without first opening the file or directory for 
    deletion.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 

CsvFs will do redirected IO for compressed files.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>



<a href="/windows/desktop/api/winbase/ns-winbase-ofstruct">OFSTRUCT</a>



<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a>