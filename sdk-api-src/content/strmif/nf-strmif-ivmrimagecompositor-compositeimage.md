---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

