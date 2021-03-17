---
UID: NF:lzexpand.LZInit
title: LZInit function (lzexpand.h)
description: Allocates memory for the internal data structures required to decompress files, and then creates and initializes them.
helpviewer_keywords: ["LZInit","LZInit function [Files]","_win32_lzinit","base.lzinit","fs.lzinit","lzexpand/LZInit"]
old-location: fs\lzinit.htm
tech.root: fs
ms.assetid: 53e6345a-e303-4ef6-8b4d-b9a3fcacfb13
ms.date: 12/05/2018
ms.keywords: LZInit, LZInit function [Files], _win32_lzinit, base.lzinit, fs.lzinit, lzexpand/LZInit
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
req.lib: Lz32.lib
req.dll: Lz32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LZInit
 - lzexpand/LZInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Lz32.dll
api_name:
 - LZInit
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> nor 
<a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.

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
 

There is no extended error information for this function; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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

<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>