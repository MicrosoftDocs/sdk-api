---
UID: NF:lzexpand.LZClose
title: LZClose function
author: windows-sdk-content
description: Closes a file that was opened by using the LZOpenFile function.
old-location: fs\lzclose.htm
old-project: fileio
ms.assetid: ba535eb7-8d9b-4290-af1f-495e9737cd38
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LZClose, LZClose function [Files], _win32_lzclose, base.lzclose, fs.lzclose, lzexpand/LZClose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lzexpand.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: POLICY_DNS_DOMAIN_INFO, *PPOLICY_DNS_DOMAIN_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Lz32.dll
api_name:
 - LZClose
product: Windows
targetos: Windows
req.lib: Lz32.lib
req.dll: Lz32.dll
req.irql: 
req.product: GDI+ 1.1
---

# LZClose function


## -description


Closes a file that was opened by using the 
<a href="https://msdn.microsoft.com/6ab3c81c-88f2-4b87-84b1-5b64848af043">LZOpenFile</a> function.


## -parameters




### -param hFile [in]

A handle to the file to be closed.


## -returns



This function does not return a value.




## -remarks



The handle identifying the file must be retrieved by calling the 
<a href="https://msdn.microsoft.com/6ab3c81c-88f2-4b87-84b1-5b64848af043">LZOpenFile</a> function. If the handle is retrieved by calling the 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or 
<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a> function, an error occurs.

If the file has been compressed by the Lempel-Ziv algorithm and opened by using 
<a href="https://msdn.microsoft.com/6ab3c81c-88f2-4b87-84b1-5b64848af043">LZOpenFile</a>, 
<b>LZClose</b> frees any global heap space that was allocated to expand the file.

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
 

CsvFs will do redirected IO for compressed files.





## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">File Compression and Decompression</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/6ab3c81c-88f2-4b87-84b1-5b64848af043">LZOpenFile</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>
 

 

