---
UID: NF:fileapi.GetLongPathNameW
title: GetLongPathNameW function
author: windows-sdk-content
description: Converts the specified path to its long form.
old-location: fs\getlongpathname.htm
old-project: FileIO
ms.assetid: 8ce69033-b69b-438b-a27f-938dd327c8ec
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetLongPathName, GetLongPathName function [Files], GetLongPathNameA, GetLongPathNameW, _win32_getlongpathname, base.getlongpathname, fileapi/GetLongPathName, fileapi/GetLongPathNameA, fileapi/GetLongPathNameW, fs.getlongpathname, winbase/GetLongPathName, winbase/GetLongPathNameA, winbase/GetLongPathNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLongPathNameW (Unicode) and GetLongPathNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	GetLongPathName
-	GetLongPathNameA
-	GetLongPathNameW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetLongPathNameW function


## -description


Converts the specified path to its long form.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/8523cde9-f0dd-4832-8d9d-9e68bac89344">GetLongPathNameTransacted</a> function.

For more information about file and path names, see 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.


## -parameters




### -param lpszShortPath [in]

The path to be converted.

In the ANSI version of this function, 
       <b>GetLongPathNameA</b>, the name is limited to 
       <b>MAX_PATH</b> (260) characters. To extend this limit to 32,767 wide characters, call the 
       Unicode version of the function, <b>GetLongPathNameW</b>, 
       and prepend "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>GetLongPathNameW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpszLongPath [out]

A pointer to the buffer to receive the long path.

You can use the same buffer you used for the <i>lpszShortPath</i> parameter.


### -param cchBuffer [in]

The size of the buffer <i>lpszLongPath</i> points to, in 
      <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpszLongPath</i>, not including the terminating null character.

If the <i>lpBuffer</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHARs</b>, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, such as if the file does not 
       exist, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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
    Example Code section for <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a>.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
It is possible to have access to a file or directory but not have access to some of the parent directories of 
    that file or directory. As a result, <b>GetLongPathName</b> may 
    fail when it is unable to query the parent directory of a path component to determine the long name for that 
    component. This check can be skipped for directory components that have file extensions longer than 3 characters, 
    or total lengths longer than 12 characters. For more information, see the 
    <a href="naming_a_file.htm">Short vs. Long Names</a> section of 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.

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
     Example Code section for <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a>



<a href="https://msdn.microsoft.com/8523cde9-f0dd-4832-8d9d-9e68bac89344">GetLongPathNameTransacted</a>



<a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>



<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>
 

 

