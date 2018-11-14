---
UID: NF:segment.IMSVidVideoRenderer.put_OverScan
title: IMSVidVideoRenderer::put_OverScan
author: windows-sdk-content
description: The put_OverScan method specifies the amount of clipping to perform on all sides of the video frame to cut off random video noise.
old-location: mstv\imsvidvideorenderer_put_overscan.htm
tech.root: MSTV
ms.assetid: 141df99b-4fc7-439c-953e-1fa1c544258e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_OverScan method, IMSVidVideoRenderer.put_OverScan, IMSVidVideoRenderer::put_OverScan, IMSVidVideoRendererput_OverScan, mstv.imsvidvideorenderer_put_overscan, put_OverScan, put_OverScan method [Microsoft TV Technologies], put_OverScan method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_OverScan
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
 - IMSVidVideoRenderer.put_OverScan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidVideoRenderer.put_OverScan
: 
---

# IMSVidVideoRenderer::put_OverScan


## -description


The <b>put_OverScan</b> method specifies the amount of clipping to perform on all sides of the video frame to cut off random video noise.


## -parameters




### -param lPercent [in]

Specifies the amount to clip, in hundredths of a percent. For example, 175 indicates 1.75%.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the current clipping mode is <b>sslClipByOverScan</b>, the VMR clips the video image by the specified amount. For more information, see <a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">IMSVidVideoRenderer::put_SourceSize</a>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/2c4946e6-b25c-4e6a-b640-73982c0da871">IMSVidVideoRenderer::get_OverScan</a>
 

 

