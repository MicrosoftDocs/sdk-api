---
UID: NF:wincodec.IWICJpegFrameEncode.GetAcHuffmanTable
title: IWICJpegFrameEncode::GetAcHuffmanTable (wincodec.h)
description: Retrieves a copy of the AC Huffman table for the specified scan and table. (IWICJpegFrameEncode.GetAcHuffmanTable)
helpviewer_keywords: ["GetAcHuffmanTable","GetAcHuffmanTable method [Windows Imaging Component]","GetAcHuffmanTable method [Windows Imaging Component]","IWICJpegFrameEncode interface","IWICJpegFrameEncode interface [Windows Imaging Component]","GetAcHuffmanTable method","IWICJpegFrameEncode.GetAcHuffmanTable","IWICJpegFrameEncode::GetAcHuffmanTable","wic.iwicjpegframeencode_getachuffmantable","wincodec/IWICJpegFrameEncode::GetAcHuffmanTable"]
old-location: wic\iwicjpegframeencode_getachuffmantable.htm
tech.root: wic
ms.assetid: 9ABE4C1E-52C7-4F08-8479-CB4F6FEE9ADA
ms.date: 12/05/2018
ms.keywords: GetAcHuffmanTable, GetAcHuffmanTable method [Windows Imaging Component], GetAcHuffmanTable method [Windows Imaging Component],IWICJpegFrameEncode interface, IWICJpegFrameEncode interface [Windows Imaging Component],GetAcHuffmanTable method, IWICJpegFrameEncode.GetAcHuffmanTable, IWICJpegFrameEncode::GetAcHuffmanTable, wic.iwicjpegframeencode_getachuffmantable, wincodec/IWICJpegFrameEncode::GetAcHuffmanTable
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICJpegFrameEncode::GetAcHuffmanTable
 - wincodec/IWICJpegFrameEncode::GetAcHuffmanTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICJpegFrameEncode.GetAcHuffmanTable
---

# IWICJpegFrameEncode::GetAcHuffmanTable


## -description

Retrieves a copy of the AC Huffman table for the specified scan and table.

## -parameters

### -param scanIndex

Type: <b>UINT</b>

The zero-based index of the scan for which data is retrieved.

### -param tableIndex

Type: <b>UINT</b>

The index of the AC Huffman table to retrieve.

### -param pAcHuffmanTable [out]

Type: <b><a href="/windows/desktop/direct3ddxgi/dxgi-jpeg-ac-huffman-table">DXGI_JPEG_AC_HUFFMAN_TABLE</a>*</b>

A pointer that receives the table data. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WINCODEC_ERR_INVALIDJPEGSCANINDEX </dt>
</dl>
</td>
<td width="60%">
The specified scan index is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WINCODEC_ERR_INVALIDPARAMETER</dt>
</dl>
</td>
<td width="60%">
Can occur if <i>pAcHuffmanTable</i> is NULL or if <i>tableIndex</i> does not point to a valid table slot. Check the scan header for valid table indices.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframeencode">IWICJpegFrameEncode</a>
