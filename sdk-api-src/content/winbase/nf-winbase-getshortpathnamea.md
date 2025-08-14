---
UID: NF:winbase.GetShortPathNameA
title: GetShortPathNameA function (winbase.h)
description: Retrieves the short path form of the specified path. (GetShortPathNameA)
helpviewer_keywords: ["GetShortPathName","GetShortPathName function [Files]","GetShortPathNameA","GetShortPathNameW","_win32_getshortpathname","base.getshortpathname","fileapi/GetShortPathName","fileapi/GetShortPathNameA","fileapi/GetShortPathNameW","fs.getshortpathname","winbase/GetShortPathName","winbase/GetShortPathNameA","winbase/GetShortPathNameW"]
old-location: fs\getshortpathname.htm
tech.root: fs
ms.assetid: 15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7
ms.date: 12/05/2018
ms.keywords: GetShortPathName, GetShortPathName function [Files], GetShortPathNameA, GetShortPathNameW, _win32_getshortpathname, base.getshortpathname, fileapi/GetShortPathName, fileapi/GetShortPathNameA, fileapi/GetShortPathNameW, fs.getshortpathname, winbase/GetShortPathName, winbase/GetShortPathNameA, winbase/GetShortPathNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetShortPathNameW (Unicode) and GetShortPathNameA (ANSI)
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
 - GetShortPathNameA
 - winbase/GetShortPathNameA
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetShortPathName
 - GetShortPathNameA
 - GetShortPathNameW
---

# GetShortPathNameA function


## -description

Retrieves the short path form of the specified path.

For more information about file and path names, see 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

## -parameters

### -param lpszLongPath [in]

The path string.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpszShortPath [out]

A pointer to a buffer to receive the null-terminated short form of the path that 
       <i>lpszLongPath</i> specifies.

Passing <b>NULL</b> for this parameter and zero for <i>cchBuffer</i> 
       will always return the required buffer size for a specified <i>lpszLongPath</i>.

### -param cchBuffer [in]

The size of the buffer  that <i>lpszShortPath</i> points to, in 
       <b>TCHARs</b>.

Set this parameter to zero if <i>lpszShortPath</i> is set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string that is copied to <i>lpszShortPath</i>, not including the terminating null 
       character.

If the <i>lpszShortPath</i> buffer is too small to contain the path, the return value is 
       the size of the buffer, in <b>TCHARs</b>, that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The path that the <i>lpszLongPath</i> parameter specifies does not have to be a full or 
    long path. The short form can be longer than the specified path.

If the return value is greater than the value specified in the <i>cchBuffer</i> parameter, 
    you can call the function again with a buffer that is large enough to hold the path. For an example of this case 
    in addition to using zero-length buffer for dynamic allocation, see the Example Code section.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
If the specified path is already in its short form  and conversion is not needed, the function simply copies 
    the specified path to the buffer specified by the <i>lpszShortPath</i> parameter.

You can set the <i>lpszShortPath</i> parameter to the same value as the 
    <i>lpszLongPath</i> parameter; in other words, you can set the output buffer for the short path 
    to the address of the input path string. Always ensure that the <i>cchBuffer</i> parameter 
    accurately represents the total size, in <b>TCHARs</b>, of this buffer.

You can obtain the long name of a file from the short name by calling the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a> function. Alternatively, where 
    <b>GetLongPathName</b> is not available, you can call 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> on each component of the path to get the 
    corresponding long name.

It is possible to have access to a file or directory but not have access to some of the parent directories of 
    that file or directory. As a result, <b>GetShortPathName</b> 
    may fail when it is unable to query the parent directory of a path component  to determine the short name for that 
    component. This check can be skipped for directory components that already meet the requirements of a short name. 
    For more information, see the 
    <a href="/windows/desktop/FileIO/naming-a-file">Short vs. Long Names</a> section of 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

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
Yes

</td>
</tr>
</table>
 

SMB 3.0 does not support short names on shares with continuous availability capability.

Resilient File System (ReFS) doesn't support short names. If you call <b>GetShortPathName</b> on a path that doesn't have any short names on-disk, the call will succeed, but will return the long-name path instead. This outcome is also possible with NTFS volumes because there's no guarantee that a short name will exist for a given long name.


#### Examples

For an example that uses <b>GetShortPathName</b>, see 
     the Example Code section for <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>.

<div class="code"></div>
The following C++ example shows how to use a dynamically allocated output buffer.


```cpp
//...
    long     length = 0;
    TCHAR*   buffer = NULL;

// First obtain the size needed by passing NULL and 0.

    length = GetShortPathName(lpszPath, NULL, 0);
    if (length == 0) ErrorExit(TEXT("GetShortPathName"));

// Dynamically allocate the correct size 
// (terminating null char was included in length)

    buffer = new TCHAR[length];

// Now simply call again using same long path.

    length = GetShortPathName(lpszPath, buffer, length);
    if (length == 0) ErrorExit(TEXT("GetShortPathName"));

    _tprintf(TEXT("long name = %s shortname = %s"), lpszPath, buffer);
    
    delete [] buffer;
///...

```

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a>



<a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfileshortnamea">SetFileShortName</a>
