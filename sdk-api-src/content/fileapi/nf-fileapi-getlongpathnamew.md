---
UID: NF:fileapi.GetLongPathNameW
title: GetLongPathNameW function (fileapi.h)
description: Converts the specified path to its long form. (Unicode)
helpviewer_keywords: ["GetLongPathName", "GetLongPathName function [Files]", "GetLongPathNameW", "_win32_getlongpathname", "base.getlongpathname", "fileapi/GetLongPathName", "fileapi/GetLongPathNameW", "fs.getlongpathname"]
old-location: fs\getlongpathname.htm
tech.root: fs
ms.assetid: 8ce69033-b69b-438b-a27f-938dd327c8ec
ms.date: 11/25/2019
ms.keywords: GetLongPathName, GetLongPathName function [Files], GetLongPathNameA, GetLongPathNameW, _win32_getlongpathname, base.getlongpathname, fileapi/GetLongPathName, fileapi/GetLongPathNameA, fileapi/GetLongPathNameW, fs.getlongpathname, winbase/GetLongPathName, winbase/GetLongPathNameA, winbase/GetLongPathNameW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLongPathNameW (Unicode) and GetLongPathNameA (ANSI)
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
 - GetLongPathNameW
 - fileapi/GetLongPathNameW
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
 - GetLongPathName
 - GetLongPathNameA
 - GetLongPathNameW
---

# GetLongPathNameW function


## -description

Converts the specified path to its long form.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getlongpathnametransacteda">GetLongPathNameTransacted</a> function.

For more information about file and path names, see 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

> [!IMPORTANT]  
> To use this function, the caller must have the following permissions on the specified path and parent directories:  
> - List Folder
> - Read Data
> - Read Attributes

## -parameters

### -param lpszShortPath [in]

The path to be converted.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpszLongPath [out]

A pointer to the buffer to receive the long path.

You can use the same buffer you used for the <i>lpszShortPath</i> parameter.

### -param cchBuffer [in]

The size of the buffer <i>lpszLongPath</i> points to, in 
      <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpszLongPath</i>, not including the terminating null character.

If the <i>lpszLongPath</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHARs</b>, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, such as if the file does not 
       exist, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

On many file systems, a short file name contains a tilde (~) character. However, not all file systems follow 
    this convention. Therefore, do not assume that you can skip calling 
    <b>GetLongPathName</b> if the path does not contain a tilde (~) 
    character.

If the file or directory exists but a long path is not found, 
    <b>GetLongPathName</b> succeeds, having copied the string 
    referred to by the <i>lpszShortPath</i> parameter to the buffer referred to by the 
    <i>lpszLongPath</i> parameter.

If the return value is greater than the value specified in <i>cchBuffer</i>, you can call 
    the function again with a buffer that is large enough to hold the path. For an example of this case, see the 
    Example Code section for <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
It is possible to have access to a file or directory but not have access to some of the parent directories of 
    that file or directory. As a result, <b>GetLongPathName</b> may 
    fail when it is unable to query the parent directory of a path component to determine the long name for that 
    component. This check can be skipped for directory components that have file extensions longer than 3 characters, 
    or total lengths longer than 12 characters. For more information, see the 
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

For an example that uses <b>GetLongPathName</b>, see the 
     Example Code section for <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines GetLongPathName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getlongpathnametransacteda">GetLongPathNameTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a>



<a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>
