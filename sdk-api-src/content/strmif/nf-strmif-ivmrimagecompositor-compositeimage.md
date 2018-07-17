---
UID: NF:strmif.IVMRImageCompositor.CompositeImage
title: IVMRImageCompositor::CompositeImage
author: windows-sdk-content
description: The CompositeImage method composites the current frames available in each input stream.
old-location: dshow\ivmrimagecompositor_compositeimage.htm
old-project: DirectShow
ms.assetid: 5af73543-d391-404a-9797-8fbb3f24879c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CompositeImage, CompositeImage method [DirectShow], CompositeImage method [DirectShow],IVMRImageCompositor interface, IVMRImageCompositor interface [DirectShow],CompositeImage method, IVMRImageCompositor.CompositeImage, IVMRImageCompositor::CompositeImage, IVMRImageCompositorCompositeImage, dshow.ivmrimagecompositor_compositeimage, strmif/IVMRImageCompositor::CompositeImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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


### -param dwClrBkGnd




### -param pVideoStreamInfo [in]

Pointer to an array of video stream info objects.


### -param cStreams [in]

Specifies the number of streams to be mixed, which is equal to the size of the pVideoStreamInfo array.


#### - clrBkgnd [in]

Specifies the background color.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

