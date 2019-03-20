---
UID: NF:fileapi.GetTempPathW
title: GetTempPathW function (fileapi.h)
author: windows-sdk-content
description: Retrieves the path of the directory designated for temporary files.
old-location: fs\gettemppath.htm
tech.root: FileIO
ms.assetid: fb366f0d-df6b-44c2-92c9-b7a8e2583054
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTempPath, GetTempPath function [Files], GetTempPathA, GetTempPathW, _win32_gettemppath, base.gettemppath, fileapi/GetTempPath, fileapi/GetTempPathA, fileapi/GetTempPathW, fs.gettemppath, winbase/GetTempPath, winbase/GetTempPathA, winbase/GetTempPathW
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTempPathW (Unicode) and GetTempPathA (ANSI)
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetTempPath
 - GetTempPathA
 - GetTempPathW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTempPathW function


## -description


Retrieves the path of the directory designated for temporary files.


## -parameters




### -param nBufferLength [in]

The size of the string buffer identified by <i>lpBuffer</i>, in 
      <b>TCHARs</b>.


### -param lpBuffer [out]

A pointer to a string buffer that receives the null-terminated string specifying the temporary file path. 
      The returned string ends with a backslash, for example, "C:\TEMP\".


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpBuffer</i>, not including the terminating null character. If the 
       return value is greater than <i>nBufferLength</i>, the return value is the length, in 
       <b>TCHARs</b>, of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The maximum possible return value is <b>MAX_PATH</b>+1 (261).




## -remarks



The <b>GetTempPath</b> function checks for the existence of 
    environment variables in the following order and uses the first path found:

<ol>
<li>The path specified by the TMP environment variable.</li>
<li>The path specified by the TEMP environment variable.</li>
<li>The path specified by the USERPROFILE environment variable.</li>
<li>The Windows directory.</li>
</ol>
Note that the function does not verify that the path exists, nor does it test to see if the current process has 
     any kind of access rights to the path. The <b>GetTempPath</b> 
     function returns the properly formatted string that specifies the fully qualified path based on the environment 
     variable search order as previously specified. The application should verify the existence of the path and 
     adequate access rights to the path prior to any use for file I/O operations.

Symbolic link behavior—If the path points to a symbolic link, the temp path name 
    maintains any symbolic links.

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

For an example, see 
     <a href="https://msdn.microsoft.com/6254c67d-5d34-499d-b1a4-8cac526dd294">Creating and Using a Temporary File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/0a30055f-a3b9-439f-9304-40ee8a07b967">GetTempFileName</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

