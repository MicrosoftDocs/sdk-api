---
UID: NF:segment.IMSVidVideoRenderer.put__CustomCompositorClass
title: IMSVidVideoRenderer::put__CustomCompositorClass
author: windows-sdk-content
description: The put__CustomCompositorClass method specifies the class identifier (CLSID) of a custom image compositor, as a GUID.
old-location: mstv\imsvidvideorenderer_put__customcompositorclass.htm
tech.root: MSTV
ms.assetid: 031af4a5-6eed-44c9-9b0c-f472d709db66
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__CustomCompositorClass method, IMSVidVideoRenderer.put__CustomCompositorClass, IMSVidVideoRenderer::put__CustomCompositorClass, IMSVidVideoRendererput__CustomCompositorClass, mstv.imsvidvideorenderer_put__customcompositorclass, put__CustomCompositorClass, put__CustomCompositorClass method [Microsoft TV Technologies], put__CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__CustomCompositorClass
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
 - IMSVidVideoRenderer.put__CustomCompositorClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::put__CustomCompositorClass


## -description


The <b>put__CustomCompositorClass</b> method specifies the class identifier (CLSID) of a custom image compositor, as a <b>GUID</b>.


## -parameters




### -param CompositorCLSID [in]

Specifies the CLSID of the custom compositor.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/0ac48bbb-a0d3-4c37-9f3e-4f4cc79b550b">IMSVidVideoRenderer::get__CustomCompositorClass</a>



<a href="https://msdn.microsoft.com/ff99b253-20bc-4b8e-8624-ffcbb3b91857">IMSVidVideoRenderer::put__CustomCompositor</a>
 

 

