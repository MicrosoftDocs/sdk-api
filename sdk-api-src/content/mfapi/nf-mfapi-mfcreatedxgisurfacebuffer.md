---
UID: NF:mfapi.MFCreateDXGISurfaceBuffer
title: MFCreateDXGISurfaceBuffer function (mfapi.h)
description: Creates a media buffer to manage a Microsoft DirectX Graphics Infrastructure (DXGI) surface.
helpviewer_keywords: ["MFCreateDXGISurfaceBuffer","MFCreateDXGISurfaceBuffer function [Media Foundation]","mf.mfcreatedxgisurfacebuffer","mfapi/MFCreateDXGISurfaceBuffer"]
old-location: mf\mfcreatedxgisurfacebuffer.htm
tech.root: mf
ms.assetid: 5D859F36-A82B-488B-A2F6-C697A1AA86BC
ms.date: 12/05/2018
ms.keywords: MFCreateDXGISurfaceBuffer, MFCreateDXGISurfaceBuffer function [Media Foundation], mf.mfcreatedxgisurfacebuffer, mfapi/MFCreateDXGISurfaceBuffer
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
 - MFCreateDXGISurfaceBuffer
 - mfapi/MFCreateDXGISurfaceBuffer
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
 - MFCreateDXGISurfaceBuffer
---

# MFCreateDXGISurfaceBuffer function


## -description

Creates a media buffer to manage a Microsoft DirectX Graphics Infrastructure (DXGI) surface.

## -parameters

### -param riid [in]

Identifies the type of DXGI surface. This value must be <b>IID_ID3D11Texture2D</b> or <b>IID_ID3D12Resource</b>.

### -param punkSurface [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the DXGI surface.

### -param uSubresourceIndex [in]

The zero-based index of a subresource of the surface. The media buffer object is associated with this subresource.

### -param fBottomUpWhenLinear [in]

If <b>TRUE</b>, the buffer's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-contiguouscopyto">IMF2DBuffer::ContiguousCopyTo</a> method copies the buffer into a bottom-up format. The bottom-up format is compatible with GDI for uncompressed RGB images. If this parameter is <b>FALSE</b>, the <b>ContiguousCopyTo</b> method copies the buffer into a top-down format, which is compatible with Direct3D.
          

For more information about top-down versus bottom-up images, see <a href="/windows/desktop/medfound/image-stride">Image Stride</a>.

### -param ppBuffer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. The caller must release the buffer.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The returned buffer object supports the following interfaces:

<ul>
<li>
<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>
</li>
<li>
<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a>
</li>
<li>
<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer">IMFDXGIBuffer</a>
</li>
<li>
<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>