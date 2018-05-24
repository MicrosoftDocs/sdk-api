---
UID: NF:segment.IMSVidVideoRenderer.get_SourceSize
title: IMSVidVideoRenderer::get_SourceSize
author: windows-driver-content
description: The get_SourceSize method retrieves the type of clipping to apply to the video rectangle, if any.
old-location: mstv\imsvidvideorenderer_get_sourcesize.htm
old-project: mstv
ms.assetid: 312a2c1e-5332-4a2d-ada9-1dc8236f4170
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_SourceSize method, IMSVidVideoRenderer.get_SourceSize, IMSVidVideoRenderer::get_SourceSize, IMSVidVideoRendererget_SourceSize, get_SourceSize, get_SourceSize method [Microsoft TV Technologies], get_SourceSize method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_sourcesize, segment/IMSVidVideoRenderer::get_SourceSize
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
-	IMSVidVideoRenderer.get_SourceSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get_SourceSize


## -description


The <b>get_SourceSize</b> method retrieves the type of clipping to apply to the video rectangle, if any.


## -parameters




### -param CurrentSize






#### - pCurrentSize

Receives a member of the <a href="https://msdn.microsoft.com/579c4993-6238-47c7-b61c-398568c1fb94">SourceSizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">IMSVidVideoRenderer::put_SourceSize</a>
 

 

