---
UID: NF:segment.IMSVidVideoRenderer.put_SourceSize
title: IMSVidVideoRenderer::put_SourceSize
author: windows-sdk-content
description: The put_SourceSize method specifies the type of clipping to apply to the video rectangle, if any.
old-location: mstv\imsvidvideorenderer_put_sourcesize.htm
old-project: mstv
ms.assetid: c792f064-a137-4872-8c79-6e924b6023f0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_SourceSize method, IMSVidVideoRenderer.put_SourceSize, IMSVidVideoRenderer::put_SourceSize, IMSVidVideoRendererput_SourceSize, mstv.imsvidvideorenderer_put_sourcesize, put_SourceSize, put_SourceSize method [Microsoft TV Technologies], put_SourceSize method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_SourceSize
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
 - IMSVidVideoRenderer.put_SourceSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidVideoRenderer::put_SourceSize


## -description


The <b>put_SourceSize</b> method specifies the type of clipping to apply to the video rectangle, if any.


## -parameters




### -param NewSize [in]

Specifies a member of the <a href="https://msdn.microsoft.com/579c4993-6238-47c7-b61c-398568c1fb94">SourceSizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/312a2c1e-5332-4a2d-ada9-1dc8236f4170">IMSVidVideoRenderer::get_SourceSize</a>



<a href="https://msdn.microsoft.com/c72d8134-ff6c-46b4-b567-35638aef53cd">IMSVidVideoRenderer::put_ClippedSourceRect</a>



<a href="https://msdn.microsoft.com/141df99b-4fc7-439c-953e-1fa1c544258e">IMSVidVideoRenderer::put_OverScan</a>
 

 

