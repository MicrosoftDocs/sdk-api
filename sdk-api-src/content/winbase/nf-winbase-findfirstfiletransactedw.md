---
UID: NF:winbase.FindFirstFileTransactedW
title: FindFirstFileTransactedW function
author: windows-sdk-content
description: Searches a directory for a file or subdirectory with a name that matches a specific name as a transacted operation.
old-location: fs\findfirstfiletransacted.htm
old-project: FileIO
ms.assetid: d94bf32b-f14b-44b4-824b-ed453d0424ef
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FIND_FIRST_EX_CASE_SENSITIVE, FindFirstFileTransacted, FindFirstFileTransacted function [Files], FindFirstFileTransactedA, FindFirstFileTransactedW, fs.findfirstfiletransacted, winbase/FindFirstFileTransacted, winbase/FindFirstFileTransactedA, winbase/FindFirstFileTransactedW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstFileTransactedW (Unicode) and FindFirstFileTransactedA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	Kernel32Legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	FindFirstFileTransacted
-	FindFirstFileTransactedA
-	FindFirstFileTransactedW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindFirstFileTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Searches a directory for a file or subdirectory with a name that matches a specific name as a 
    transacted operation.

This function is the transacted form of the <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function.

For the most basic version of this function, see <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>.


## -parameters




### -param lpFileName [in]

The directory or path, and the file name. The file name can include wildcard characters,  for example, an asterisk 
       (*) or a question mark (?).

This parameter should not be <b>NULL</b>, an invalid string (for example, an empty string or a string that is missing the terminating null character), or end in a trailing backslash (\).

If the string ends with a wildcard, period (.), or directory name, the user must have access to the root and 
       all subdirectories on the path.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. To extend this limit to 
       32,767 wide characters, call the Unicode version of the function and prepend "\\?\" to the 
       path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param fInfoLevelId [in]

The information level of the returned data.
      

This parameter is one of the 
       <a href="https://msdn.microsoft.com/454d5fc2-2ada-49de-9e1e-9e6eba050b17">FINDEX_INFO_LEVELS</a> enumeration values.


### -param lpFindFileData [out]

A pointer to the <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure that 
       receives information about a found file or subdirectory.


### -param fSearchOp [in]

The type of filtering to perform that is different from wildcard matching.
      

This parameter is one of the <a href="https://msdn.microsoft.com/3f4c18fb-e128-421f-bd05-456d4d3698a7">FINDEX_SEARCH_OPS</a> 
       enumeration values.


### -param lpSearchFilter

A pointer to the search criteria if the specified <i>fSearchOp</i> needs structured search 
       information.
      

At this time, none of the supported <i>fSearchOp</i> values require extended search 
       information. Therefore, this pointer must be <b>NULL</b>.


### -param dwAdditionalFlags [in]

Specifies additional flags that control the search.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FIND_FIRST_EX_CASE_SENSITIVE"></a><a id="find_first_ex_case_sensitive"></a><dl>
<dt><b>FIND_FIRST_EX_CASE_SENSITIVE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Searches are case-sensitive.

</td>
</tr>
</table>
 


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is a search handle used in a subsequent call to 
       <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> or 
       <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>, and  the <i>lpFindFileData</i> parameter contains information about the first file or directory found.

If the function fails or fails to locate files from the search string in the <i>lpFileName</i> parameter, the return value is <b>INVALID_HANDLE_VALUE</b> and the contents of <i>lpFindFileData</i> are indeterminate. To get extended 
       error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The <b>FindFirstFileTransacted</b> function opens a search handle and 
    returns information about the first file that the file system finds with a name that matches the specified pattern. This may or may not be the first file or directory that appears in a directory-listing application (such as the dir command) when given the same file name string pattern. This is because <b>FindFirstFileTransacted</b> does no sorting of the search results. For additional information, see <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>.

The following list 
    identifies some other search characteristics:

<ul>
<li>The search is performed strictly on the name of the file, not on any attributes such as a date or a file 
      type.</li>
<li>The search includes the long and short file names.</li>
<li>An attempt to open 
    a search with a trailing backslash always fails.</li>
<li>Passing an invalid string, <b>NULL</b>, or empty string for the <i>lpFileName</i> parameter is not a valid use of this function. Results in this case are undefined.</li>
</ul>
<div class="alert"><b>Note</b>  In rare cases, file information on NTFS file systems may not be current at the time you call this 
    function. To be assured of getting the current file information, call  the 
    <a href="https://msdn.microsoft.com/d026ee3a-c165-42a2-a4e1-efccdafbefc5">GetFileInformationByHandle</a> function.</div>
<div> </div>
If the underlying file system does not support the specified type of filtering, other than directory 
    filtering, <b>FindFirstFileTransacted</b>fails with the error 
    <b>ERROR_NOT_SUPPORTED</b>. The application must use 
    <a href="https://msdn.microsoft.com/3f4c18fb-e128-421f-bd05-456d4d3698a7">FINDEX_SEARCH_OPS</a> type 
    <b>FileExSearchNameMatch</b> and perform its own filtering.

After the search handle is established, use it in the 
    <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> function to search for other 
    files that match the same pattern with the same filtering that is being performed. When the search handle is not 
    needed, it should be closed by using the 
    <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a> function.

As stated previously, you cannot use a trailing backslash (\) in the <i>lpFileName</i> input string for 
    <b>FindFirstFileTransacted</b>, therefore it may not be obvious how to search root directories. If you want to see files or get the attributes of a root directory, the following options would apply:

<ul>
<li>To examine files in a root directory, you can use "C:\*" and step through the directory by 
      using <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>.</li>
<li>To get the attributes of a root directory, use 
      the <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function.</li>
</ul>
<div class="alert"><b>Note</b>  Prepending the string "\\?\" does not allow access to the root directory.</div>
<div> </div>
On network shares, you can use an <i>lpFileName</i> in the form of the following: 
    "\\server\service\*". However, you cannot use an <i>lpFileName</i> that points to 
    the share itself; for example, "\\server\service" is not valid.

To examine a directory that is not a root directory, use the path to that directory, without a trailing 
    backslash. For example, an argument of "C:\Windows" returns information about the directory 
    "C:\Windows", not about a directory or file in "C:\Windows". To examine the files and directories in "C:\Windows", use an <i>lpFileName</i> of "C:\Windows\*".

Be aware that some other thread or process could create or delete a file with this name between the time you query for the result 
    and the time you act on the information. If this is a potential concern for your application,  one possible solution is to use the 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with 
    <b>CREATE_NEW</b> (which fails if the file exists) or <b>OPEN_EXISTING</b> (which fails 
    if the file does not exist).

If you are writing a 32-bit application to list all the files in a directory and the application may be run on 
    a 64-bit computer, you should call 
    <a href="https://msdn.microsoft.com/44bedfa3-5a92-4e78-9e38-8278a7efe9b7">Wow64DisableWow64FsRedirection</a> before 
    calling <b>FindFirstFileTransacted</b> and call <a href="https://msdn.microsoft.com/8a09bdeb-b969-48b2-a432-c78dd4177000">Wow64RevertWow64FsRedirection</a> after the last call to <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>. For more information, see <a href="https://msdn.microsoft.com/b4d36fe8-8bbb-469b-8ad1-650d559a4c75">File System Redirector</a>.

If the path points to a symbolic link, the 
    <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> buffer contains information about 
    the symbolic link, not the target.

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
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 

SMB 3.0 does not support TxF.




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/3d5400c3-555f-44fc-9470-52a36d04d90b">SetFileAttributes</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>



<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>
 

 

