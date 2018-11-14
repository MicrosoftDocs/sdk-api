---
UID: NF:fileapi.FindFirstFileW
title: FindFirstFileW function
author: windows-sdk-content
description: Searches a directory for a file or subdirectory with a name that matches a specific name (or partial name if wildcards are used).
old-location: fs\findfirstfile.htm
tech.root: fileio
ms.assetid: 02fc92c4-582d-4c9f-a811-b5c839e9fffa
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FindFirstFile, FindFirstFile function [Files], FindFirstFileA, FindFirstFileW, _win32_findfirstfile, base.findfirstfile, fileapi/FindFirstFile, fileapi/FindFirstFileA, fileapi/FindFirstFileW, fs.findfirstfile, winbase/FindFirstFile, winbase/FindFirstFileA, winbase/FindFirstFileW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FindFirstFileW
: 
---

# FindFirstFileW function


## -description


Searches a directory for a file or subdirectory with a name that matches a specific name (or partial 
    name if wildcards are used).

To specify additional attributes to use in a search, use the 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/d94bf32b-f14b-44b4-824b-ed453d0424ef">FindFirstFileTransacted</a> function.


## -parameters




### -param lpFileName [in]

The directory or path, and the file name. The file name can include wildcard characters,  for example, an asterisk 
       (*) or a question mark (?).

This parameter should not be <b>NULL</b>, an invalid string (for example, an empty string 
       or a string that is missing the terminating null character), or end in a trailing backslash (\).

If the string ends with a wildcard, period (.), or directory name, the user must have access permissions to 
       the root and all subdirectories on the path.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>FindFirstFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

### -param lpFindFileData [out]

A pointer to the <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure that 
      receives information about a found file or directory.


## -returns



If the function succeeds, the return value is a search handle used in a subsequent call to 
       <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> or 
       <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>, and  the 
       <i>lpFindFileData</i> parameter contains information about the first file or directory 
       found.

If the function fails or fails to locate files from the search string in the 
       <i>lpFileName</i> parameter, the return value is 
       <b>INVALID_HANDLE_VALUE</b> and the contents of <i>lpFindFileData</i> are 
       indeterminate. To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

If the function fails because no matching files can be found, the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns 
       <b>ERROR_FILE_NOT_FOUND</b>.




## -remarks



The <b>FindFirstFile</b> function opens a search handle and 
    returns information about the first file that the file system finds with a name that matches the specified 
    pattern. This may or may not be the first file or directory that appears in a directory-listing application (such 
    as the dir command) when given the same file name string pattern. This is because 
    <b>FindFirstFile</b> does no sorting of the search results. For 
    additional information, see <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>.

The following list identifies some other search characteristics:

<ul>
<li>The search is performed strictly on the name of the file, not on any attributes such as a date or a file 
      type (for other options, see <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>).</li>
<li>The search includes the long and short file names.</li>
<li>An attempt to open a search with a trailing backslash always fails.</li>
<li>Passing an invalid string, <b>NULL</b>, or empty string for the 
      <i>lpFileName</i> parameter is not a valid use of this function. Results in this case are 
      undefined.</li>
</ul>
<div class="alert"><b>Note</b>  In rare cases or on a heavily loaded system, file attribute information on NTFS file systems may not be 
    current at the time this function is called. To be assured of getting the current NTFS file system file 
    attributes, call the 
    <a href="https://msdn.microsoft.com/d026ee3a-c165-42a2-a4e1-efccdafbefc5">GetFileInformationByHandle</a> function.</div>
<div> </div>
After the search handle is established, you can use it to search for other files that match the same pattern 
    by using the <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> function.

When the search handle is no longer needed, close it by using the 
    <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a> function, not 
    <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.

As stated previously, you cannot use a trailing backslash (\) in the <i>lpFileName</i> 
    input string for <b>FindFirstFile</b>, therefore it may not be 
    obvious how to search root directories. If you want to see files or get the attributes of a root directory, the 
    following options would apply:

<ul>
<li>To examine files in a root directory, you can use "C:\*" and step through the 
      directory by using <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>.</li>
<li>To get the attributes of a root directory, use the 
      <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function.</li>
</ul>
<div class="alert"><b>Note</b>  Prepending the string "\\?\" does not allow access to the root 
     directory.</div>
<div> </div>
On network shares, you can use an <i>lpFileName</i> in the form of the following: 
    "\\Server\Share\*". However, you cannot use an <i>lpFileName</i> 
    that points to the share itself; for example, "\\Server\Share" is not valid.

To examine a directory that is not a root directory, use the path to that directory, without a trailing 
    backslash. For example, an argument of "C:\Windows" returns information about the 
    directory "C:\Windows", not about a directory or file in 
    "C:\Windows". To examine the files and directories in 
    "C:\Windows", use an <i>lpFileName</i> of 
    "C:\Windows\*".

Be aware that some other thread or process could create or delete a file with this name between the time you 
    query for the result and the time you act on the information. If this is a potential concern for your application, 
    one possible solution is to use the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with 
    <b>CREATE_NEW</b> (which fails if the file exists) or <b>OPEN_EXISTING</b> 
    (which fails if the file does not exist).

If you are writing a 32-bit application to list all the files in a directory and the application may be  run 
    on a 64-bit computer, you should call the 
    <a href="https://msdn.microsoft.com/44bedfa3-5a92-4e78-9e38-8278a7efe9b7">Wow64DisableWow64FsRedirection</a>function 
    before calling <b>FindFirstFile</b> and call 
    <a href="https://msdn.microsoft.com/8a09bdeb-b969-48b2-a432-c78dd4177000">Wow64RevertWow64FsRedirection</a> after the 
    last call to <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>. For more information, see 
    <a href="https://msdn.microsoft.com/b4d36fe8-8bbb-469b-8ad1-650d559a4c75">File System Redirector</a>.

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
     <a href="https://msdn.microsoft.com/ab0d977d-f71c-4a18-9b1d-2221169324f0">Listing the Files in a Directory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>



<a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>



<a href="https://msdn.microsoft.com/d94bf32b-f14b-44b4-824b-ed453d0424ef">FindFirstFileTransacted</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/3d5400c3-555f-44fc-9470-52a36d04d90b">SetFileAttributes</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>



<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>
 

 

