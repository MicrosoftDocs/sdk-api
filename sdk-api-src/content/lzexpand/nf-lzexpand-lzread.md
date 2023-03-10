---
UID: NF:lzexpand.LZRead
title: LZRead function (lzexpand.h)
description: Reads (at most) the specified number of bytes from a file and copies them into a buffer.
helpviewer_keywords: ["LZRead","LZRead function [Files]","_win32_lzread","base.lzread","fs.lzread","lzexpand/LZRead"]
old-location: fs\lzread.htm
tech.root: fs
ms.assetid: 15c6829f-2e24-4299-a2fa-a5737ec73ba9
ms.date: 12/05/2018
ms.keywords: LZRead, LZRead function [Files], _win32_lzread, base.lzread, fs.lzread, lzexpand/LZRead
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
 - LZRead
 - lzexpand/LZRead
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
 - LZRead
---

# LZRead function


## -description

Reads (at most) the specified number of bytes from a file and copies them into a buffer.

## -parameters

### -param hFile [in]

A handle to the file.

### -param lpBuffer [out]

A pointer to a buffer that receives the bytes read from the file. Ensure that this buffer is larger than <i>cbRead</i>.

### -param cbRead [in]

The count of bytes to be read.

## -returns

If the function succeeds, the return value specifies the number of bytes read.

If the function fails, the return value is an LZERROR_* code. These codes have values less than zero. Note that 
<b>LZRead</b> calls neither <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> nor <a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.

The following is the list of error codes that 
<b>LZRead</b> can return upon failure.

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
<dt><b>LZERROR_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
One of the input parameters is not valid.

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
<tr>
<td width="40%">
<dl>
<dt><b>LZERROR_WRITE</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient space for the output file.

</td>
</tr>
</table>
 

There is no extended error information for this function; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The handle identifying the file must be retrieved by calling either the 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzinit">LZInit</a> or 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a> function.

If the file is compressed, 
<b>LZRead</b> operates on an expanded image of the file and copies the bytes of data into the specified buffer.

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



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzseek">LZSeek</a>