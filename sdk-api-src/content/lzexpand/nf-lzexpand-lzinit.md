---
UID: NF:lzexpand.LZInit
title: LZInit function
author: windows-sdk-content
description: Allocates memory for the internal data structures required to decompress files, and then creates and initializes them.
old-location: fs\lzinit.htm
old-project: FileIO
ms.assetid: 53e6345a-e303-4ef6-8b4d-b9a3fcacfb13
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: LZInit, LZInit function [Files], _win32_lzinit, base.lzinit, fs.lzinit, lzexpand/LZInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lzexpand.h
req.include-header: Windows.h
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Lz32.dll
api_name:
-	LZInit
product: Windows
targetos: Windows
req.lib: Lz32.lib
req.dll: Lz32.dll
req.irql: 
req.product: GDI+ 1.1
---

# LZInit function


## -description


Allocates memory for the internal data structures required to decompress files, and then creates and initializes them.


## -parameters




### -param hfSource [in]

A handle to the file.


## -returns



If the function succeeds, the return value is a new LZ file handle.

If the function fails, the return value is an LZERROR_* code. These codes have values less than zero. Note that 
<b>LZInit</b> calls neither 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> nor 
<a href="https://msdn.microsoft.com/d97494db-868a-49d4-a613-e8beba86d4e6">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.

The following is the list of the error codes that 
<b>LZInit</b> can return upon failure.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_BADINHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle identifying the source file is not valid. The file cannot be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_GLOBALLOC</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of open compressed files has been exceeded or local memory cannot be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_GLOBLOCK</b></dt>
</dl>
</td>
<td width="60%">
The LZ file handle cannot be locked down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_UNKNOWNALG</b></dt>
</dl>
</td>
<td width="60%">
The file is compressed with an unrecognized compression algorithm.

</td>
</tr>
</table>
 

There is no extended error information for this function; do not call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A maximum of 16 compressed files can be open at any given time. Similarly, a maximum of 16 uncompressed files can be open at any given time. An application should be careful to close the handle returned by 
<b>LZInit</b> when it is done using the file; otherwise, the application can inadvertently hit the 16-file limit.

The handle this function returns is compatible only with the functions in Lz32.dll; it should not be used for other file operations.

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




<a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">File Compression and Decompression</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>
 

 

