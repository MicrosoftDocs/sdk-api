---
UID: NF:compressapi.CreateCompressor
title: CreateCompressor function (compressapi.h)
description: Generates a new COMPRESSOR_HANDLE.
helpviewer_keywords: ["COMPRESS_ALGORITHM_LZMS","COMPRESS_ALGORITHM_MSZIP","COMPRESS_ALGORITHM_XPRESS","COMPRESS_ALGORITHM_XPRESS_HUFF","CreateCompressor","CreateCompressor function [Compression API]","cmpapi.createcompressor","compressapi/CreateCompressor"]
old-location: cmpapi\createcompressor.htm
tech.root: cmpapi
ms.assetid: 782b3c08-158a-4bbd-89a5-c20666cbfb94
ms.date: 12/05/2018
ms.keywords: COMPRESS_ALGORITHM_LZMS, COMPRESS_ALGORITHM_MSZIP, COMPRESS_ALGORITHM_XPRESS, COMPRESS_ALGORITHM_XPRESS_HUFF, CreateCompressor, CreateCompressor function [Compression API], cmpapi.createcompressor, compressapi/CreateCompressor
req.header: compressapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateCompressor
 - compressapi/CreateCompressor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - cabinet.dll
api_name:
 - CreateCompressor
---

# CreateCompressor function


## -description

Generates a new <b>COMPRESSOR_HANDLE</b>.

## -parameters

### -param Algorithm [in]

The type of compression algorithm and mode to be used by this compressor.


This parameter can have one of the following values optionally combined with the <b>COMPRESS_RAW</b> flag.  Use a "bitwise OR" operator to include <b>COMPRESS_RAW</b> and to create a  block mode compressor.  If <b>COMPRESS_RAW</b> is not included, the Compression API creates a buffer mode compressor. For more information about selecting a compression algorithm and mode, see <a href="/windows/desktop/cmpapi/using-the-compression-api">Using the Compression API</a>.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMPRESS_ALGORITHM_MSZIP"></a><a id="compress_algorithm_mszip"></a><dl>
<dt><b>COMPRESS_ALGORITHM_MSZIP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
MSZIP compression algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="COMPRESS_ALGORITHM_XPRESS"></a><a id="compress_algorithm_xpress"></a><dl>
<dt><b>COMPRESS_ALGORITHM_XPRESS</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
XPRESS compression algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="COMPRESS_ALGORITHM_XPRESS_HUFF"></a><a id="compress_algorithm_xpress_huff"></a><dl>
<dt><b>COMPRESS_ALGORITHM_XPRESS_HUFF</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
XPRESS compression algorithm with Huffman encoding

</td>
</tr>
<tr>
<td width="40%"><a id="COMPRESS_ALGORITHM_LZMS"></a><a id="compress_algorithm_lzms"></a><dl>
<dt><b>COMPRESS_ALGORITHM_LZMS</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
LZMS compression algorithm

</td>
</tr>
</table>

### -param AllocationRoutines [in, optional]

Optional memory allocation and deallocation routines in a <a href="/windows/win32/api/compressapi/ns-compressapi-compress_allocation_routines">COMPRESS_ALLOCATION_ROUTINES</a> structure.

### -param CompressorHandle [out]

If the function succeeds, the handle to the specified compressor.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.  If the system can find no compression algorithm matching the specified name and version, the error  can be <b>ERROR_NOT_SUPPORTED</b>.

## -see-also

<a href="/windows/win32/api/compressapi/ns-compressapi-compress_allocation_routines">COMPRESS_ALLOCATION_ROUTINES</a>



<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>