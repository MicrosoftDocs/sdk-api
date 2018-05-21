---
UID: NF:segment.IMSVidVideoRenderer.put__CustomCompositor
title: IMSVidVideoRenderer::put__CustomCompositor
author: windows-driver-content
description: The put__CustomCompositor method specifies a custom image compositor for the Video Mixing Renderer (VMR) to use.
old-location: mstv\imsvidvideorenderer_put__customcompositor.htm
old-project: mstv
ms.assetid: ff99b253-20bc-4b8e-8624-ffcbb3b91857
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__CustomCompositor method, IMSVidVideoRenderer.put__CustomCompositor, IMSVidVideoRenderer::put__CustomCompositor, IMSVidVideoRendererput__CustomCompositor, mstv.imsvidvideorenderer_put__customcompositor, put__CustomCompositor, put__CustomCompositor method [Microsoft TV Technologies], put__CustomCompositor method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__CustomCompositor
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.put__CustomCompositor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRenderer::put__CustomCompositor


## -description


The <b>put__CustomCompositor</b> method specifies a custom image compositor for the Video Mixing Renderer (VMR) to use.


## -parameters




### -param Compositor






#### - pCompositor [in]

Pointer to the <a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor</a> interface of the image compositor.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/cafdc512-2994-4374-9396-b0bb946bc490">IMSVidVideoRenderer::get__CustomCompositor</a>



<a href="https://msdn.microsoft.com/031af4a5-6eed-44c9-9b0c-f472d709db66">IMSVidVideoRenderer::put__CustomCompositorClass</a>
 

 

