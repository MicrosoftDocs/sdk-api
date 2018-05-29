---
UID: NF:fileapi.FindNextStreamW
title: FindNextStreamW function
author: windows-sdk-content
description: Continues a stream search started by a previous call to the FindFirstStreamW function.
old-location: fs\findnextstreamw.htm
old-project: FileIO
ms.assetid: 2bb0301c-b2be-4056-913c-e4102386135e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FindNextStreamW, FindNextStreamW function [Files], _win32_findnextstreamw, base.findnextstreamw, fileapi/FindNextStreamW, fs.findnextstreamw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
-	API-MS-Win-Core-File-l1-2-2.dll
-	KernelBase.dll
-	MinKernelBase.dll
api_name:
-	FindNextStreamW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FindNextStreamW function


## -description


Continues a stream search started by a previous call to the 
    <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> function.


## -parameters




### -param hFindStream [in]

The search handle returned by a previous call to the 
      <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> function.


### -param lpFindStreamData [out]

A pointer to the 
      <a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a> structure that 
      receives information about the stream.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If no  more streams can be found, 
       <b>GetLastError</b> returns 
       <b>ERROR_HANDLE_EOF</b> (38).




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
 




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a>



<a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a>
 

 

