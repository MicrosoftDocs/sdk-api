---
UID: NF:fileapi.FindFirstFileW
title: FindFirstFileW function (fileapi.h)
description: Searches a directory for a file or subdirectory with a name that matches a specific name (or partial name if wildcards are used). (Unicode)
helpviewer_keywords: ["FindFirstFile", "FindFirstFile function [Files]", "FindFirstFileW", "_win32_findfirstfile", "base.findfirstfile", "fileapi/FindFirstFile", "fileapi/FindFirstFileW", "fs.findfirstfile"]
old-location: fs\findfirstfile.htm
tech.root: fs
ms.assetid: 02fc92c4-582d-4c9f-a811-b5c839e9fffa
ms.date: 12/05/2018
ms.keywords: FindFirstFile, FindFirstFile function [Files], FindFirstFileA, FindFirstFileW, _win32_findfirstfile, base.findfirstfile, fileapi/FindFirstFile, fileapi/FindFirstFileA, fileapi/FindFirstFileW, fs.findfirstfile, winbase/FindFirstFile, winbase/FindFirstFileA, winbase/FindFirstFileW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstFileW (Unicode) and FindFirstFileA (ANSI)
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
 - FindFirstFileW
 - fileapi/FindFirstFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FindFirstFile
 - FindFirstFileA
 - FindFirstFileW
---

# FindFirstFileW function


## -description

Searches a directory for a file or subdirectory with a name that matches a specific name (or partial 
    name if wildcards are used).

To specify additional attributes to use in a search, use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexw">FindFirstFileEx</a> function.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransactedw">FindFirstFileTransacted</a> function.

## -parameters

### -param lpFileName [in]

The directory or path, and the file name. The file name can include wildcard characters,  for example, an asterisk 
       (*) or a question mark (?).

This parameter should not be <b>NULL</b>, an invalid string (for example, an empty string 
       or a string that is missing the terminating null character), or end in a trailing backslash (\\).

If the string ends with a wildcard, period (.), or directory name, the user must have access permissions to 
       the root and all subdirectories on the path.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpFindFileData [out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure that 
      receives information about a found file or directory.

## -returns

If the function succeeds, the return value is a search handle used in a subsequent call to 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a> or 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>, and  the 
       <i>lpFindFileData</i> parameter contains information about the first file or directory 
       found.

If the function fails or fails to locate files from the search string in the 
       <i>lpFileName</i> parameter, the return value is 
       <b>INVALID_HANDLE_VALUE</b> and the contents of <i>lpFindFileData</i> are 
       indeterminate. To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If the function fails because no matching files can be found, the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
       <b>ERROR_FILE_NOT_FOUND</b>.

## -remarks

The <b>FindFirstFile</b> function opens a search handle and 
    returns information about the first file that the file system finds with a name that matches the specified 
    pattern. This may or may not be the first file or directory that appears in a directory-listing application (such 
    as the dir command) when given the same file name string pattern. This is because 
    <b>FindFirstFile</b> does no sorting of the search results. For 
    additional information, see <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a>.

The following list identifies some other search characteristics:

<ul>
<li>The search is performed strictly on the name of the file, not on any attributes such as a date or a file 
      type (for other options, see <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexw">FindFirstFileEx</a>).</li>
<li>The search includes the long and short file names.</li>
<li>An attempt to open a search with a trailing backslash always fails.</li>
<li>Passing an invalid string, <b>NULL</b>, or empty string for the 
      <i>lpFileName</i> parameter is not a valid use of this function. Results in this case are 
      undefined.</li>
</ul>
<div class="alert"><b>Note</b>  In rare cases or on a heavily loaded system, file attribute information on NTFS file systems may not be 
    current at the time this function is called. To be assured of getting the current NTFS file system file 
    attributes, call the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> function.</div>
<div> </div>
After the search handle is established, you can use it to search for other files that match the same pattern 
    by using the <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a> function.

When the search handle is no longer needed, close it by using the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function, not 
    <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

As stated previously, you cannot use a trailing backslash (\\) in the <i>lpFileName</i> 
    input string for <b>FindFirstFile</b>, therefore it may not be 
    obvious how to search root directories. If you want to see files or get the attributes of a root directory, the 
    following options would apply:

<ul>
<li>To examine files in a root directory, you can use "C:\*" and step through the 
      directory by using <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a>.</li>
<li>To get the attributes of a root directory, use the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesw">GetFileAttributes</a> function.</li>
</ul>
<div class="alert"><b>Note</b>  Prepending the string "\\?\" does not allow access to the root 
     directory.</div>
<div> </div>

On network shares, you can use an <i>lpFileName</i> in the form of the following: 
    "\\\\Server\\Share\\*". However, you cannot use an <i>lpFileName</i> 
    that points to the share itself; for example, "\\\\Server\\Share" is not valid.

To examine a directory that is not a root directory, use the path to that directory, without a trailing 
    backslash. For example, an argument of "C:\\Windows" returns information about the 
    directory "C:\\Windows", not about a directory or file in 
    "C:\\Windows". To examine the files and directories in 
    "C:\\Windows", use an <i>lpFileName</i> of 
    "C:\\Windows\\*".

Be aware that some other thread or process could create or delete a file with this name between the time you 
    query for the result and the time you act on the information. If this is a potential concern for your application, 
    one possible solution is to use the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilew">CreateFile</a> function with 
    <b>CREATE_NEW</b> (which fails if the file exists) or <b>OPEN_EXISTING</b> 
    (which fails if the file does not exist).

If you are writing a 32-bit application to list all the files in a directory and the application may be  run 
    on a 64-bit computer, you should call the 
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> function 
    before calling <b>FindFirstFile</b> and call 
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a> after the 
    last call to <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a>. For more information, see 
    <a href="/windows/desktop/WinProg64/file-system-redirector">File System Redirector</a>.

If the path points to a symbolic link, the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataw">WIN32_FIND_DATA</a> buffer contains information about 
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
 


#### Examples

The following C++ example shows you a minimal use of <b>FindFirstFile</b>.


```cpp
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void _tmain(int argc, TCHAR *argv[])
{
   WIN32_FIND_DATA FindFileData;
   HANDLE hFind;

   if( argc != 2 )
   {
      _tprintf(TEXT("Usage: %s [target_file]\n"), argv[0]);
      return;
   }

   _tprintf (TEXT("Target file is %s\n"), argv[1]);
   hFind = FindFirstFile(argv[1], &FindFileData);
   if (hFind == INVALID_HANDLE_VALUE) 
   {
      printf ("FindFirstFile failed (%d)\n", GetLastError());
      return;
   } 
   else 
   {
      _tprintf (TEXT("The first file found is %s\n"), 
                FindFileData.cFileName);
      FindClose(hFind);
   }
}

```


For another example, see 
     <a href="/windows/desktop/FileIO/listing-the-files-in-a-directory">Listing the Files in a Directory</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines FindFirstFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexw">FindFirstFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransactedw">FindFirstFileTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesw">GetFileAttributes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesw">SetFileAttributes</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataw">WIN32_FIND_DATA</a>
