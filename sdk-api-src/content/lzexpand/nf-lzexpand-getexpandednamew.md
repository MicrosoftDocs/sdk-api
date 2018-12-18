---
UID: NF:lzexpand.GetExpandedNameW
title: GetExpandedNameW function
author: windows-sdk-content
description: Retrieves the original name of a compressed file, if the file was compressed by the Lempel-Ziv algorithm.
old-location: fs\getexpandedname.htm
tech.root: fileio
ms.assetid: 173344bc-59ba-46ba-901a-f8a8929bc4ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetExpandedName, GetExpandedName function [Files], GetExpandedNameA, GetExpandedNameW, _win32_getexpandedname, base.getexpandedname, fs.getexpandedname, lzexpand/GetExpandedName, lzexpand/GetExpandedNameA, lzexpand/GetExpandedNameW
ms.topic: function
req.header: lzexpand.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetExpandedNameW (Unicode) and GetExpandedNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Lz32.lib
req.dll: Lz32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Lz32.dll
api_name:
 - GetExpandedName
 - GetExpandedNameA
 - GetExpandedNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetExpandedNameW function


## -description


Retrieves the original name of a compressed file, if the file was compressed by the Lempel-Ziv algorithm.


## -parameters




### -param lpszSource [in]

The name of the compressed file.


### -param lpszBuffer [out]

A pointer to a buffer that receives the original name of the compressed file.


## -returns



If the function succeeds, the return value is 1.

If the function fails, the return value is LZERROR_BADVALUE. There is no extended error information for this function; do not call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  <b>GetExpandedName</b> calls neither 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> nor 
<a href="https://msdn.microsoft.com/d97494db-868a-49d4-a613-e8beba86d4e6">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.</div>
<div> </div>



## -remarks



The contents of the buffer pointed to by the <i>lpszBuffer</i> parameter is the original file name if the file was compressed by using the <b>/r</b> option. If the <b>/r</b> option was not used, this function duplicates the name in the <i>lpszSource</i> parameter into the <i>lpszBuffer</i> buffer.

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




<a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">File Compression and Decompression</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>
 

 

