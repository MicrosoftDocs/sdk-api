---
UID: NF:segment.IMSVidVideoRenderer.get__CustomCompositor
title: IMSVidVideoRenderer::get__CustomCompositor
author: windows-sdk-content
description: The get__CustomCompositor method retrieves the Video Mixing Renderer's current image compositor.
old-location: mstv\imsvidvideorenderer_get__customcompositor.htm
old-project: mstv
ms.assetid: cafdc512-2994-4374-9396-b0bb946bc490
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__CustomCompositor method, IMSVidVideoRenderer.get__CustomCompositor, IMSVidVideoRenderer::get__CustomCompositor, IMSVidVideoRendererget__CustomCompositor, get__CustomCompositor, get__CustomCompositor method [Microsoft TV Technologies], get__CustomCompositor method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__customcompositor, segment/IMSVidVideoRenderer::get__CustomCompositor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get__CustomCompositor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidVideoRenderer::get__CustomCompositor


## -description


The <b>get__CustomCompositor</b> method retrieves the Video Mixing Renderer's current image compositor.


## -parameters




### -param Compositor






#### - ppCompositor [out]

Receives an <a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor</a> interface pointer .


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>.

The returned <a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/0ac48bbb-a0d3-4c37-9f3e-4f4cc79b550b">IMSVidVideoRenderer::get__CustomCompositorClass</a>



<a href="https://msdn.microsoft.com/ff99b253-20bc-4b8e-8624-ffcbb3b91857">IMSVidVideoRenderer::put__CustomCompositor</a>
 

 

