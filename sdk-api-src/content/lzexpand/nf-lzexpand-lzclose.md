---
UID: NF:lzexpand.LZClose
title: LZClose function (lzexpand.h)
description: Closes a file that was opened by using the LZOpenFile function.
helpviewer_keywords: ["LZClose","LZClose function [Files]","_win32_lzclose","base.lzclose","fs.lzclose","lzexpand/LZClose"]
old-location: fs\lzclose.htm
tech.root: fs
ms.assetid: ba535eb7-8d9b-4290-af1f-495e9737cd38
ms.date: 12/05/2018
ms.keywords: LZClose, LZClose function [Files], _win32_lzclose, base.lzclose, fs.lzclose, lzexpand/LZClose
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
 - LZClose
 - lzexpand/LZClose
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
 - LZClose
---

# LZClose function


## -description

Closes a file that was opened by using the 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a> function.

## -parameters

### -param hFile [in]

A handle to the file to be closed.

## -remarks

The handle identifying the file must be retrieved by calling the 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a> function. If the handle is retrieved by calling the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a> function, an error occurs.

If the file has been compressed by the Lempel-Ziv algorithm and opened by using 
<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a>, 
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

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/lzexpand/nf-lzexpand-lzopenfilea">LZOpenFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>