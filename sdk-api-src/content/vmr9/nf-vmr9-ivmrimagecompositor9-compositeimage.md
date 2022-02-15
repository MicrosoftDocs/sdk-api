---
UID: NF:vmr9.IVMRImageCompositor9.CompositeImage
title: IVMRImageCompositor9::CompositeImage (vmr9.h)
description: The CompositeImage method composites the current frames available in each input stream.
helpviewer_keywords: ["CompositeImage","CompositeImage method [DirectShow]","CompositeImage method [DirectShow]","IVMRImageCompositor9 interface","IVMRImageCompositor9 interface [DirectShow]","CompositeImage method","IVMRImageCompositor9.CompositeImage","IVMRImageCompositor9::CompositeImage","IVMRImageCompositor9CompositeImage","dshow.ivmrimagecompositor9_compositeimage","vmr9/IVMRImageCompositor9::CompositeImage"]
old-location: dshow\ivmrimagecompositor9_compositeimage.htm
tech.root: dshow
ms.assetid: a59d21e8-faa2-484d-9d82-991c6bc4e045
ms.date: 12/05/2018
ms.keywords: CompositeImage, CompositeImage method [DirectShow], CompositeImage method [DirectShow],IVMRImageCompositor9 interface, IVMRImageCompositor9 interface [DirectShow],CompositeImage method, IVMRImageCompositor9.CompositeImage, IVMRImageCompositor9::CompositeImage, IVMRImageCompositor9CompositeImage, dshow.ivmrimagecompositor9_compositeimage, vmr9/IVMRImageCompositor9::CompositeImage
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRImageCompositor9::CompositeImage
 - vmr9/IVMRImageCompositor9::CompositeImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRImageCompositor9.CompositeImage
---

# IVMRImageCompositor9::CompositeImage


## -description

The <code>CompositeImage</code> method composites the current frames available in each input stream.

## -parameters

### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.

### -param pddsRenderTarget [in]

Specifies the Direct3D surface that all drawing should be performed on.

### -param pmtRenderTarget [in]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that contains the media type of the target surface.

### -param rtStart [in]

Specifies the start time.

### -param rtEnd [in]

Specifies the end time.

### -param dwClrBkGnd [in]

Specifies the background color, as a <b>D3DCOLOR</b> type.

### -param pVideoStreamInfo [in]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9videostreaminfo">VMR9VideoStreamInfo</a> structures, which describe each video stream.

### -param cStreams [in]

Specifies the number of streams to mix, which is also the size of the <i>pVideoStreamInfo</i> array.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagecompositor9">IVMRImageCompositor9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>