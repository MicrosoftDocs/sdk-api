---
UID: NF:fileapi.FindFirstFileNameW
title: FindFirstFileNameW function
author: windows-sdk-content
description: Creates an enumeration of all the hard links to the specified file. The FindFirstFileNameW function returns a handle to the enumeration that can be used on subsequent calls to the FindNextFileNameW function.
old-location: fs\findfirstfilenamew.htm
tech.root: fileio
ms.assetid: 9f64aa3e-4c73-47a8-8304-6134f1b4d153
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FindFirstFileNameW, FindFirstFileNameW function [Files], fileapi/FindFirstFileNameW, fs.findfirstfilenamew
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-L1-2-2.dll
 - KernelBase.dll
api_name:
 - FindFirstFileNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindFirstFileNameW function


## -description


Creates an enumeration of all the hard links to the specified file. The 
    <b>FindFirstFileNameW</b> function returns a handle to the 
    enumeration that can be used on subsequent calls to the 
    <a href="https://msdn.microsoft.com/1d2f8041-2744-4f37-afde-ddce49a8bdc5">FindNextFileNameW</a> function.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/79c7d32d-3cb7-4e27-9db1-f24282bf606a">FindFirstFileNameTransactedW</a> function.


## -parameters




### -param lpFileName [in]

The name of the file.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param dwFlags [in]

Reserved; specify zero (0).


### -param StringLength [in, out]

The size of the buffer pointed to by the <i>LinkName</i> parameter, in characters. If 
      this call fails and the error returned from the 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function is 
      <b>ERROR_MORE_DATA</b> (234), the value that is returned by this parameter is the size that 
      the buffer pointed to by <i>LinkName</i>  must be to contain all the data.


### -param LinkName [in, out]

A pointer to a buffer to store the first link name found for <i>lpFileName</i>.


## -returns



If the function succeeds, the return value is a search handle that can be used with the 
       <a href="https://msdn.microsoft.com/1d2f8041-2744-4f37-afde-ddce49a8bdc5">FindNextFileNameW</a> function or closed with the 
       <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a> function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b> (0xffffffff). To 
       get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
       function.




## -remarks



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
 




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>



<a href="https://msdn.microsoft.com/79c7d32d-3cb7-4e27-9db1-f24282bf606a">FindFirstFileNameTransactedW</a>



<a href="https://msdn.microsoft.com/1d2f8041-2744-4f37-afde-ddce49a8bdc5">FindNextFileNameW</a>
 

 

