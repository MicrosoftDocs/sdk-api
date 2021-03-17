---
UID: NF:lzexpand.LZCopy
title: LZCopy function (lzexpand.h)
description: Copies a source file to a destination file.
helpviewer_keywords: ["LZCopy","LZCopy function [Files]","_win32_lzcopy","base.lzcopy","fs.lzcopy","lzexpand/LZCopy"]
old-location: fs\lzcopy.htm
tech.root: fs
ms.assetid: 9b6e1ab7-68a2-4721-9e84-11c4126f37a7
ms.date: 12/05/2018
ms.keywords: LZCopy, LZCopy function [Files], _win32_lzcopy, base.lzcopy, fs.lzcopy, lzexpand/LZCopy
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
 - LZCopy
 - lzexpand/LZCopy
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
 - LZCopy
---

# LZCopy function


## -description

Copies a source file to a destination file. If the source file has been compressed by the Lempel-Ziv algorithm, this function creates a decompressed destination file. If the source file is not compressed, this function duplicates the original file.

## -parameters

### -param hfSource [in]

A handle to the source file.

### -param hfDest [in]

A handle to the destination file.

## -returns

If the function succeeds, the return value specifies the size, in bytes, of the destination file.

If the function fails, the return value is an LZERROR_* code. These codes have values less than zero. Note that 
<b>LZCopy</b> calls neither 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> nor 
<a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.

The following is a list of error codes that 
<b>LZCopy</b> can return upon failure.

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
<dt><b>LZERROR_BADOUTHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle identifying the destination file is not valid. The file cannot be written.

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
<dt><b>LZERROR_READ</b></dt>
</dl>
</td>
<td width="60%">
The source file format is not valid.

</td>
</tr>
</table>
 

There is no extended error information for this function; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The handles identifying the source and destination files must be retrieved by calling the 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzinit">LZInit</a> or 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a> function. 

If the function succeeds, the file identified by the <i>hfDest</i> parameter is always uncompressed.

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



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzinit">LZInit</a>



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a>