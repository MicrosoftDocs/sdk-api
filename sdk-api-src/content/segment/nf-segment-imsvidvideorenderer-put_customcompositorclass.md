---
UID: NF:segment.IMSVidVideoRenderer.put_CustomCompositorClass
title: IMSVidVideoRenderer::put_CustomCompositorClass
author: windows-driver-content
description: The put_CustomCompositorClass method specifies the class identifier (CLSID) of a custom image compositor, as a BSTR.
old-location: mstv\imsvidvideorenderer_put_customcompositorclass.htm
old-project: mstv
ms.assetid: 399a5151-b26a-4c33-9dd9-e7abb23cbd1c
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_CustomCompositorClass method, IMSVidVideoRenderer.put_CustomCompositorClass, IMSVidVideoRenderer::put_CustomCompositorClass, IMSVidVideoRendererput_CustomCompositorClass, mstv.imsvidvideorenderer_put_customcompositorclass, put_CustomCompositorClass, put_CustomCompositorClass method [Microsoft TV Technologies], put_CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_CustomCompositorClass
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
-	IMSVidVideoRenderer.put_CustomCompositorClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRenderer::put_CustomCompositorClass


## -description


The <b>put_CustomCompositorClass</b> method specifies the class identifier (CLSID) of a custom image compositor, as a <b>BSTR</b>.


## -parameters




### -param CompositorCLSID [in]

Specifies the CLSID as a string.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is provided for Automation clients. C++ applications can use the <a href="https://msdn.microsoft.com/031af4a5-6eed-44c9-9b0c-f472d709db66">IMSVidVideoRenderer::put__CustomCompositorClass</a> method, which specifies a <b>GUID</b> rather than a <b>BSTR</b>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/d6ff1968-e891-432d-9271-f6d6a6a8a756">IMSVidVideoRenderer::get_CustomCompositorClass</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

