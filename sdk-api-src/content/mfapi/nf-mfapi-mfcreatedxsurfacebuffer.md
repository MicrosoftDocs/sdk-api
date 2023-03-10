---
UID: NF:mfapi.MFCreateDXSurfaceBuffer
title: MFCreateDXSurfaceBuffer function (mfapi.h)
description: Creates a media buffer object that manages a Direct3D 9 surface.
helpviewer_keywords: ["MFCreateDXSurfaceBuffer","MFCreateDXSurfaceBuffer function [Media Foundation]","d1ee158e-5d70-41a4-b746-2ecaea2db92c","mf.mfcreatedxsurfacebuffer","mfapi/MFCreateDXSurfaceBuffer"]
old-location: mf\mfcreatedxsurfacebuffer.htm
tech.root: mf
ms.assetid: d1ee158e-5d70-41a4-b746-2ecaea2db92c
ms.date: 12/05/2018
ms.keywords: MFCreateDXSurfaceBuffer, MFCreateDXSurfaceBuffer function [Media Foundation], d1ee158e-5d70-41a4-b746-2ecaea2db92c, mf.mfcreatedxsurfacebuffer, mfapi/MFCreateDXSurfaceBuffer
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Evr.lib
req.dll: Evr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateDXSurfaceBuffer
 - mfapi/MFCreateDXSurfaceBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - evr.dll
api_name:
 - MFCreateDXSurfaceBuffer
---

# MFCreateDXSurfaceBuffer function


## -description

Creates a media buffer object that manages a Direct3D 9 surface.

## -parameters

### -param riid [in]

Identifies the type of Direct3D 9 surface. Currently this value must be <b>IID_IDirect3DSurface9</b>.

### -param punkSurface [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the DirectX surface.

### -param fBottomUpWhenLinear [in]

If <b>TRUE</b>, the buffer's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-contiguouscopyto">IMF2DBuffer::ContiguousCopyTo</a> method copies the buffer into a bottom-up format. The bottom-up format is compatible with GDI for uncompressed RGB images. If this parameter is <b>FALSE</b>, the <b>ContiguousCopyTo</b> method copies the buffer into a top-down format, which is compatible with DirectX.
          

For more information about top-down versus bottom-up images, see <a href="/windows/desktop/medfound/image-stride">Image Stride</a>.

### -param ppBuffer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. The caller must release the buffer.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

This function creates a media buffer object that holds a pointer to the Direct3D surface specified in <i>punkSurface</i>. Locking the buffer gives the caller access to the surface memory. When the buffer object is destroyed, it releases the surface. For more information about media buffers, see <a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>.

<div class="alert"><b>Note</b>  This function does not allocate the Direct3D surface itself.</div>
<div> </div>
The buffer object created by this function also exposes the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface. For more information, see <a href="/windows/desktop/medfound/directx-surface-buffer">DirectX Surface Buffer</a>.
      

This function does not support DXGI surfaces.

## -see-also

<a href="/windows/desktop/medfound/directx-surface-buffer">DirectX Surface Buffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>