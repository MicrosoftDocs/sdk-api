---
UID: NF:segment.IMSVidVideoRenderer.get_MaxVidRect
title: IMSVidVideoRenderer::get_MaxVidRect
author: windows-sdk-content
description: The get_MaxVidRect method retrieves the maximum ideal size of the video rectangle.
old-location: mstv\imsvidvideorenderer_get_maxvidrect.htm
old-project: mstv
ms.assetid: b4c4b2da-0749-463c-aaa1-04d0d456327a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MaxVidRect method, IMSVidVideoRenderer.get_MaxVidRect, IMSVidVideoRenderer::get_MaxVidRect, IMSVidVideoRendererget_MaxVidRect, get_MaxVidRect, get_MaxVidRect method [Microsoft TV Technologies], get_MaxVidRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_maxvidrect, segment/IMSVidVideoRenderer::get_MaxVidRect
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.get_MaxVidRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get_MaxVidRect


## -description


The <b>get_MaxVidRect</b> method retrieves the maximum ideal size of the video rectangle.


## -parameters




### -param ppVidRect [out]

Receives an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The maximum ideal image size is the maximum video size that can be displayed without significantly degrading performance or image quality.

The returned <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/2e65f2b2-d479-429a-b5c7-8c5cbb6c833d">IMSVidVideoRenderer::get_MinVidRect</a>
 

 

