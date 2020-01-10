---
UID: NF:strmif.IVMRImageCompositor.CompositeImage
title: IVMRImageCompositor::CompositeImage (strmif.h)
description: The CompositeImage method composites the current frames available in each input stream.
old-location: dshow\ivmrimagecompositor_compositeimage.htm
tech.root: DirectShow
ms.assetid: 5af73543-d391-404a-9797-8fbb3f24879c
ms.date: 12/05/2018
ms.keywords: CompositeImage, CompositeImage method [DirectShow], CompositeImage method [DirectShow],IVMRImageCompositor interface, IVMRImageCompositor interface [DirectShow],CompositeImage method, IVMRImageCompositor.CompositeImage, IVMRImageCompositor::CompositeImage, IVMRImageCompositorCompositeImage, dshow.ivmrimagecompositor_compositeimage, strmif/IVMRImageCompositor::CompositeImage
f1_keywords:
- strmif/IVMRImageCompositor.CompositeImage
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRImageCompositor.CompositeImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRImageCompositor::CompositeImage


## -description



The <code>CompositeImage</code> method composites the current frames available in each input stream.




## -parameters




### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device. The compositor must cast this to a <b>LPDIRECT3DDEVICE7</b> type.


### -param pddsRenderTarget [in]

Specifies the DirectDraw surface that all drawing should be performed on.


### -param pmtRenderTarget [in]

Specifies the media type of the DirectDraw surface.


### -param rtStart [in]

Specifies the start time.


### -param rtEnd [in]

Specifies the end time.


### -param dwClrBkGnd [in]

Specifies the background color.


### -param pVideoStreamInfo [in]

Pointer to an array of video stream info objects.


### -param cStreams [in]

Specifies the number of streams to be mixed, which is equal to the size of the pVideoStreamInfo array.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

