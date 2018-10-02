---
UID: NF:segment.IMSVidVideoRenderer.get_OverScan
title: IMSVidVideoRenderer::get_OverScan
author: windows-sdk-content
description: The get_OverScan method retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.
old-location: mstv\imsvidvideorenderer_get_overscan.htm
tech.root: MSTV
ms.assetid: 2c4946e6-b25c-4e6a-b640-73982c0da871
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_OverScan method, IMSVidVideoRenderer.get_OverScan, IMSVidVideoRenderer::get_OverScan, IMSVidVideoRendererget_OverScan, get_OverScan, get_OverScan method [Microsoft TV Technologies], get_OverScan method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_overscan, segment/IMSVidVideoRenderer::get_OverScan
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
 - IMSVidVideoRenderer.get_OverScan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::get_OverScan


## -description


The <b>get_OverScan</b> method retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.


## -parameters




### -param plPercent [out]

Receives the amount to clip, in hundredths of a percent.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the current clipping mode is <b>sslClipByOverScan</b>, the VMR clips the video image by the amount given in the <i>plPercent</i> parameter. For more information, see <a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">IMSVidVideoRenderer::put_SourceSize</a>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/141df99b-4fc7-439c-953e-1fa1c544258e">IMSVidVideoRenderer::put_OverScan</a>
 

 

