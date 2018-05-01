---
UID: NF:segment.IMSVidVideoRenderer.get_AvailableSourceRect
title: IMSVidVideoRenderer::get_AvailableSourceRect method
author: windows-driver-content
description: The get_AvailableSourceRect method retrieves the size of the native video.
old-location: mstv\imsvidvideorenderer_get_availablesourcerect.htm
old-project: mstv
ms.assetid: 33747e97-3e1c-4220-89c9-cc8310b77c4e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidVideoRenderer, IMSVidVideoRenderer interface [Microsoft TV Technologies], get_AvailableSourceRect method, IMSVidVideoRenderer::get_AvailableSourceRect, IMSVidVideoRendererget_AvailableSourceRect, get_AvailableSourceRect method [Microsoft TV Technologies], get_AvailableSourceRect method [Microsoft TV Technologies], IMSVidVideoRenderer interface, get_AvailableSourceRect,IMSVidVideoRenderer.get_AvailableSourceRect, mstv.imsvidvideorenderer_get_availablesourcerect, segment/IMSVidVideoRenderer::get_AvailableSourceRect
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
-	IMSVidVideoRenderer.get_AvailableSourceRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRenderer::get_AvailableSourceRect method


## -description


The <b>get_AvailableSourceRect</b> method retrieves the size of the native video.


## -parameters




### -param pRect






#### - ppRect [out]

Receives an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The returned <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>
 

 

