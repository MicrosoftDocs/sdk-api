---
UID: NF:fileapi.FindClose
title: FindClose function
author: windows-driver-content
description: Closes a file search handle opened by the FindFirstFile, FindFirstFileEx, FindFirstFileNameW, FindFirstFileNameTransactedW, FindFirstFileTransacted, FindFirstStreamTransactedW, or FindFirstStreamW functions.
old-location: fs\findclose.htm
old-project: FileIO
ms.assetid: 64b3bc49-1e0e-4572-9d9f-936c45f5b01c
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: FindClose, FindClose function [Files], _win32_findclose, base.findclose, fileapi/FindClose, fs.findclose, winbase/FindClose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
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
-	FindClose
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FindClose function


## -description


Closes a file search handle opened by the 
    <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>, 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>, 
    <a href="https://msdn.microsoft.com/9f64aa3e-4c73-47a8-8304-6134f1b4d153">FindFirstFileNameW</a>, 
    <a href="https://msdn.microsoft.com/79c7d32d-3cb7-4e27-9db1-f24282bf606a">FindFirstFileNameTransactedW</a>, 
    <a href="https://msdn.microsoft.com/d94bf32b-f14b-44b4-824b-ed453d0424ef">FindFirstFileTransacted</a>, 
    <a href="https://msdn.microsoft.com/76c64aa9-0501-457d-b774-c209fbac4ccc">FindFirstStreamTransactedW</a>, or 
    <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> functions.


## -parameters




### -param hFindFile [in, out]

The file search handle. 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After the <b>FindClose</b> function is called, the handle 
    specified by the <i>hFindFile</i> parameter cannot be used in subsequent calls to the 
    <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>, 
    <a href="https://msdn.microsoft.com/1d2f8041-2744-4f37-afde-ddce49a8bdc5">FindNextFileNameW</a>, 
    <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>, or 
    <b>FindClose</b> functions.

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
     <a href="https://msdn.microsoft.com/ab0d977d-f71c-4a18-9b1d-2221169324f0">Listing the Files in a Directory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>



<a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>



<a href="https://msdn.microsoft.com/79c7d32d-3cb7-4e27-9db1-f24282bf606a">FindFirstFileNameTransactedW</a>



<a href="https://msdn.microsoft.com/9f64aa3e-4c73-47a8-8304-6134f1b4d153">FindFirstFileNameW</a>



<a href="https://msdn.microsoft.com/d94bf32b-f14b-44b4-824b-ed453d0424ef">FindFirstFileTransacted</a>



<a href="https://msdn.microsoft.com/76c64aa9-0501-457d-b774-c209fbac4ccc">FindFirstStreamTransactedW</a>



<a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/1d2f8041-2744-4f37-afde-ddce49a8bdc5">FindNextFileNameW</a>



<a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>
 

 

