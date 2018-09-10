---
UID: NF:segment.IMSVidVideoRenderer.get__CustomCompositorClass
title: IMSVidVideoRenderer::get__CustomCompositorClass
author: windows-sdk-content
description: The get__CustomCompositorClass method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a GUID.
old-location: mstv\imsvidvideorenderer_get__customcompositorclass.htm
tech.root: mstv
ms.assetid: 0ac48bbb-a0d3-4c37-9f3e-4f4cc79b550b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__CustomCompositorClass method, IMSVidVideoRenderer.get__CustomCompositorClass, IMSVidVideoRenderer::get__CustomCompositorClass, IMSVidVideoRendererget__CustomCompositorClass, get__CustomCompositorClass, get__CustomCompositorClass method [Microsoft TV Technologies], get__CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__customcompositorclass, segment/IMSVidVideoRenderer::get__CustomCompositorClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get__CustomCompositorClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::get__CustomCompositorClass


## -description


The <b>get__CustomCompositorClass</b> method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a <b>GUID</b>.


## -parameters




### -param CompositorCLSID

TBD




#### - pCompositorCLSID [out]

Receives the CLSID.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/cafdc512-2994-4374-9396-b0bb946bc490">IMSVidVideoRenderer::get__CustomCompositor</a>



<a href="https://msdn.microsoft.com/031af4a5-6eed-44c9-9b0c-f472d709db66">IMSVidVideoRenderer::put__CustomCompositorClass</a>
 

 

