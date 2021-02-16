---
UID: NF:d3d11_1.ID3D11VideoProcessorEnumerator1.CheckVideoProcessorFormatConversion
title: ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion (d3d11_1.h)
description: Indicates whether the driver supports the specified combination of format and colorspace conversions.
helpviewer_keywords: ["CheckVideoProcessorFormatConversion","CheckVideoProcessorFormatConversion method [Media Foundation]","CheckVideoProcessorFormatConversion method [Media Foundation]","ID3D11VideoProcessorEnumerator1 interface","ID3D11VideoProcessorEnumerator1 interface [Media Foundation]","CheckVideoProcessorFormatConversion method","ID3D11VideoProcessorEnumerator1.CheckVideoProcessorFormatConversion","ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion","d3d11_1/ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion","mf.id3d11videoprocessorenumerator1_checkvideoprocessorformatconversion"]
old-location: mf\id3d11videoprocessorenumerator1_checkvideoprocessorformatconversion.htm
tech.root: mf
ms.assetid: 97DDE2C9-ABF2-47FB-B77C-BD1BC7AC5F2F
ms.date: 12/05/2018
ms.keywords: CheckVideoProcessorFormatConversion, CheckVideoProcessorFormatConversion method [Media Foundation], CheckVideoProcessorFormatConversion method [Media Foundation],ID3D11VideoProcessorEnumerator1 interface, ID3D11VideoProcessorEnumerator1 interface [Media Foundation],CheckVideoProcessorFormatConversion method, ID3D11VideoProcessorEnumerator1.CheckVideoProcessorFormatConversion, ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion, d3d11_1/ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion, mf.id3d11videoprocessorenumerator1_checkvideoprocessorformatconversion
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion
 - d3d11_1/ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoProcessorEnumerator1.CheckVideoProcessorFormatConversion
---

# ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion


## -description

Indicates whether the driver supports the specified combination of format and colorspace conversions.

## -parameters

### -param InputFormat [in]

Type: <b>DXGI_FORMAT</b>

The format of the video processor input.

### -param InputColorSpace [in]

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The colorspace of the video processor input.

### -param OutputFormat [in]

Type: <b>DXGI_FORMAT</b>

The format of the video processor output.

### -param OutputColorSpace [in]

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The colorspace of the video processor output.

### -param pSupported [out]

Type: <b>BOOL*</b>

Pointer to a boolean that is set by the driver to indicate if the specified combination of format and colorspace conversions is supported. True if the conversion is supported; otherwise, false.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videoprocessorenumerator1">ID3D11VideoProcessorEnumerator1</a>