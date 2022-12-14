---
UID: NF:winbase.FindFirstFileTransactedA
title: FindFirstFileTransactedA function (winbase.h)
description: Searches a directory for a file or subdirectory with a name that matches a specific name as a transacted operation. (ANSI)
helpviewer_keywords: ["FIND_FIRST_EX_CASE_SENSITIVE","FindFirstFileTransacted","FindFirstFileTransacted function [Files]","FindFirstFileTransactedA","FindFirstFileTransactedW","fs.findfirstfiletransacted","winbase/FindFirstFileTransacted","winbase/FindFirstFileTransactedA","winbase/FindFirstFileTransactedW"]
old-location: fs\findfirstfiletransacted.htm
tech.root: fs
ms.assetid: d94bf32b-f14b-44b4-824b-ed453d0424ef
ms.date: 12/05/2018
ms.keywords: FIND_FIRST_EX_CASE_SENSITIVE, FindFirstFileTransacted, FindFirstFileTransacted function [Files], FindFirstFileTransactedA, FindFirstFileTransactedW, fs.findfirstfiletransacted, winbase/FindFirstFileTransacted, winbase/FindFirstFileTransactedA, winbase/FindFirstFileTransactedW
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindFirstFileTransactedA
 - winbase/FindFirstFileTransactedA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - FindFirstFileTransacted
 - FindFirstFileTransactedA
 - FindFirstFileTransactedW
---

# FindFirstFileTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Searches a directory for a file or subdirectory with a name that matches a specific name as a 
    transacted operation.

This function is the transacted form of the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a> function.

For the most basic version of this function, see <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>.

## -parameters

### -param lpFileName [in]

The directory or path, and the file name. The file name can include wildcard characters,  for example, an asterisk 
       (*) or a question mark (?).

This parameter should not be <b>NULL</b>, an invalid string (for example, an empty string or a string that is missing the terminating null character), or end in a trailing backslash (\\).

If the string ends with a wildcard, period (.), or directory name, the user must have access to the root and 
       all subdirectories on the path.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. To extend this limit to 
       32,767 wide characters, call the Unicode version of the function and prepend "\\?\" to the 
       path. For more information, see 
       <a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param fInfoLevelId [in]

The information level of the returned data.
      

This parameter is one of the 
       <a href="/windows/desktop/api/minwinbase/ne-minwinbase-findex_info_levels">FINDEX_INFO_LEVELS</a> enumeration values.

### -param lpFindFileData [out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure that 
       receives information about a found file or subdirectory.

### -param fSearchOp [in]

The type of filtering to perform that is different from wildcard matching.
      

This parameter is one of the <a href="/windows/desktop/api/minwinbase/ne-minwinbase-findex_search_ops">FINDEX_SEARCH_OPS</a> 
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

A handle to the transaction. This handle is returned by the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is a search handle used in a subsequent call to 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a> or 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>, and  the <i>lpFindFileData</i> parameter contains information about the first file or directory found.

If the function fails or fails to locate files from the search string in the <i>lpFileName</i> parameter, the return value is <b>INVALID_HANDLE_VALUE</b> and the contents of <i>lpFindFileData</i> are indeterminate. To get extended 
       error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The <b>FindFirstFileTransacted</b> function opens a search handle and 
    returns information about the first file that the file system finds with a name that matches the specified pattern. This may or may not be the first file or directory that appears in a directory-listing application (such as the dir command) when given the same file name string pattern. This is because <b>FindFirstFileTransacted</b> does no sorting of the search results. For additional information, see <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>.

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
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> function.</div>
<div> </div>
If the underlying file system does not support the specified type of filtering, other than directory 
    filtering, <b>FindFirstFileTransacted</b> fails with the error 
    <b>ERROR_NOT_SUPPORTED</b>. The application must use 
    <a href="/windows/desktop/api/minwinbase/ne-minwinbase-findex_search_ops">FINDEX_SEARCH_OPS</a> type 
    <b>FileExSearchNameMatch</b> and perform its own filtering.

After the search handle is established, use it in the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a> function to search for other 
    files that match the same pattern with the same filtering that is being performed. When the search handle is not 
    needed, it should be closed by using the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function.

As stated previously, you cannot use a trailing backslash (\\) in the <i>lpFileName</i> input string for 
    <b>FindFirstFileTransacted</b>, therefore it may not be obvious how to search root directories. If you want to see files or get the attributes of a root directory, the following options would apply:

<ul>
<li>To examine files in a root directory, you can use "C:\*" and step through the directory by 
      using <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>.</li>
<li>To get the attributes of a root directory, use 
      the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> function.</li>
</ul>
<div class="alert"><b>Note</b>  Prepending the string "\\?\" does not allow access to the root directory.</div>
<div> </div>

On network shares, you can use an <i>lpFileName</i> in the form of the following: 
    "\\\\server\\service\*". However, you cannot use an <i>lpFileName</i> that points to 
    the share itself; for example, "\\\\server\\service" is not valid.

To examine a directory that is not a root directory, use the path to that directory, without a trailing 
    backslash. For example, an argument of "C:\\Windows" returns information about the directory 
    "C:\\Windows", not about a directory or file in "C:\\Windows". To examine the files and directories in "C:\\Windows", use an <i>lpFileName</i> of "C:\\Windows\\*".

Be aware that some other thread or process could create or delete a file with this name between the time you query for the result 
    and the time you act on the information. If this is a potential concern for your application,  one possible solution is to use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function with 
    <b>CREATE_NEW</b> (which fails if the file exists) or <b>OPEN_EXISTING</b> (which fails 
    if the file does not exist).

If you are writing a 32-bit application to list all the files in a directory and the application may be run on 
    a 64-bit computer, you should call 
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> before 
    calling <b>FindFirstFileTransacted</b> and call <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a> after the last call to <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>. For more information, see <a href="/windows/desktop/WinProg64/file-system-redirector">File System Redirector</a>.

If the path points to a symbolic link, the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> buffer contains information about 
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





> [!NOTE]
> The winbase.h header defines FindFirstFileTransacted as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a>
