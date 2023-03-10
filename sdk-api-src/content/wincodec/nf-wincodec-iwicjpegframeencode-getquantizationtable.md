---
UID: NF:wincodec.IWICJpegFrameEncode.GetQuantizationTable
title: IWICJpegFrameEncode::GetQuantizationTable (wincodec.h)
description: Retrieves a copy of the quantization table. (IWICJpegFrameEncode.GetQuantizationTable)
helpviewer_keywords: ["GetQuantizationTable","GetQuantizationTable method [Windows Imaging Component]","GetQuantizationTable method [Windows Imaging Component]","IWICJpegFrameEncode interface","IWICJpegFrameEncode interface [Windows Imaging Component]","GetQuantizationTable method","IWICJpegFrameEncode.GetQuantizationTable","IWICJpegFrameEncode::GetQuantizationTable","wic.iwicjpegframeencode_getquantizationtable","wincodec/IWICJpegFrameEncode::GetQuantizationTable"]
old-location: wic\iwicjpegframeencode_getquantizationtable.htm
tech.root: wic
ms.assetid: 6FBDAEA2-78E6-4152-815D-FA6164FE396F
ms.date: 12/05/2018
ms.keywords: GetQuantizationTable, GetQuantizationTable method [Windows Imaging Component], GetQuantizationTable method [Windows Imaging Component],IWICJpegFrameEncode interface, IWICJpegFrameEncode interface [Windows Imaging Component],GetQuantizationTable method, IWICJpegFrameEncode.GetQuantizationTable, IWICJpegFrameEncode::GetQuantizationTable, wic.iwicjpegframeencode_getquantizationtable, wincodec/IWICJpegFrameEncode::GetQuantizationTable
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
 - IWICJpegFrameEncode::GetQuantizationTable
 - wincodec/IWICJpegFrameEncode::GetQuantizationTable
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
 - IWICJpegFrameEncode.GetQuantizationTable
---

# IWICJpegFrameEncode::GetQuantizationTable


## -description

Retrieves a copy of the quantization table.

## -parameters

### -param scanIndex

Type: <b>UINT</b>

The zero-based index of the scan for which data is retrieved.

### -param tableIndex

Type: <b>UINT</b>

The index of the quantization table to retrieve.

### -param pQuantizationTable [out]

Type: <b><a href="/windows/desktop/direct3ddxgi/dxgi-jpeg-quantization-table">DXGI_JPEG_QUANTIZATION_TABLE</a>*</b>

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
Can occur if <i>pTable</i> is NULL or if <i>tableIndex</i> does not point to a valid table slot. Check the scan header for valid table indices.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframeencode">IWICJpegFrameEncode</a>
