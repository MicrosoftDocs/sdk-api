---
UID: NF:mfapi.MFCreate2DMediaBuffer
title: MFCreate2DMediaBuffer function (mfapi.h)
description: Creates a system-memory buffer object to hold 2D image data.
helpviewer_keywords: ["MFCreate2DMediaBuffer","MFCreate2DMediaBuffer function [Media Foundation]","mf.mfcreate2dmediabuffer","mfapi/MFCreate2DMediaBuffer"]
old-location: mf\mfcreate2dmediabuffer.htm
tech.root: mf
ms.assetid: 7D999070-87BD-46AF-A4F0-C0A23DC1C876
ms.date: 12/05/2018
ms.keywords: MFCreate2DMediaBuffer, MFCreate2DMediaBuffer function [Media Foundation], mf.mfcreate2dmediabuffer, mfapi/MFCreate2DMediaBuffer
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreate2DMediaBuffer
 - mfapi/MFCreate2DMediaBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreate2DMediaBuffer
---

# MFCreate2DMediaBuffer function


## -description

Creates a system-memory buffer object to hold 2D image data.

## -parameters

### -param dwWidth [in]

Width of the image, in pixels.

### -param dwHeight [in]

Height of the image, in pixels.

### -param dwFourCC [in]

A <b>FOURCC</b> code or <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> value that specifies the video format. If you have a video subtype GUID, you can use the first <b>DWORD</b> of the subtype.

### -param fBottomUp [in]

If <b>TRUE,</b> the buffer's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-contiguouscopyto">IMF2DBuffer::ContiguousCopyTo</a> method copies the buffer into a bottom-up format. The bottom-up format is compatible with GDI for uncompressed RGB images. If this parameter is <b>FALSE</b>, the <b>ContiguousCopyTo</b> method copies the buffer into a top-down format, which is compatible with DirectX. 



For more information about top-down versus bottom-up images, see <a href="/windows/desktop/medfound/image-stride">Image Stride</a>.

### -param ppBuffer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
Unrecognized video format.

</td>
</tr>
</table>

## -remarks

The returned buffer object also exposes the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a> interface.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>