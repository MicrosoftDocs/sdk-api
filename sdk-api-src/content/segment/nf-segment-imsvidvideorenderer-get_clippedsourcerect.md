---
UID: NF:segment.IMSVidVideoRenderer.get_ClippedSourceRect
title: IMSVidVideoRenderer::get_ClippedSourceRect
author: windows-sdk-content
description: The get_ClippedSourceRect method retrieves the clipping rectangle on the video source.
old-location: mstv\imsvidvideorenderer_get_clippedsourcerect.htm
tech.root: mstv
ms.assetid: d40d39d9-41a4-42e1-b0d0-4a6299fd1cff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_ClippedSourceRect method, IMSVidVideoRenderer.get_ClippedSourceRect, IMSVidVideoRenderer::get_ClippedSourceRect, IMSVidVideoRendererget_ClippedSourceRect, get_ClippedSourceRect, get_ClippedSourceRect method [Microsoft TV Technologies], get_ClippedSourceRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_clippedsourcerect, segment/IMSVidVideoRenderer::get_ClippedSourceRect
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
 - IMSVidVideoRenderer.get_ClippedSourceRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::get_ClippedSourceRect


## -description


The <b>get_ClippedSourceRect</b> method retrieves the clipping rectangle on the video source.


## -parameters




### -param pRect [out]

Receives an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the current clipping mode is <b>sslClipByClipRect</b>, the VMR clips the video image to the video source rectangle, and stretches the clipped image to fill the Video Control's video window. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd694755(v=VS.85).aspx">IMSVidVideoRenderer::put_SourceSize</a>.

The returned <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694748(v=VS.85).aspx">IMSVidVideoRenderer::put_ClippedSourceRect</a>
 

 

