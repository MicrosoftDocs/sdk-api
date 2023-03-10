---
UID: NF:lzexpand.LZSeek
title: LZSeek function (lzexpand.h)
description: Moves a file pointer the specified number of bytes from a starting position.
helpviewer_keywords: ["LZSeek","LZSeek function [Files]","_win32_lzseek","base.lzseek","fs.lzseek","lzexpand/LZSeek"]
old-location: fs\lzseek.htm
tech.root: fs
ms.assetid: eb3d8546-6280-4e4b-8ca4-3697b9339d86
ms.date: 12/05/2018
ms.keywords: LZSeek, LZSeek function [Files], _win32_lzseek, base.lzseek, fs.lzseek, lzexpand/LZSeek
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
 - LZSeek
 - lzexpand/LZSeek
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
 - LZSeek
---

# LZSeek function


## -description

Moves a file pointer the specified number of bytes from a starting position.

## -parameters

### -param hFile [in]

A handle to the file.

### -param lOffset [in]

The number of bytes by which to move the file pointer.

### -param iOrigin [in]

The starting position of the pointer. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Moves the file pointer <i>lOffset</i> bytes from the beginning of the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Moves the file pointer <i>lOffset</i> bytes from the current position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Moves the file pointer <i>lOffset</i> bytes from the end of the file.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value specifies the offset from the beginning of the file to the new pointer position.

If the function fails, the return value is an LZERROR_* code. These codes have values less than zero. Note that 
<b>LZSeek</b> calls neither <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> nor <a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.

The following is the list of error codes that 
<b>LZSeek</b> can return upon failure.

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
<dt><b>LZERROR_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is outside the range of acceptable values.

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
</table>
 

There is no extended error information for this function; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The handle identified by the <i>hFile</i> parameter must be retrieved by calling either the 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzinit">LZInit</a> or 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a> function.

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