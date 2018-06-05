---
UID: NF:segment.IMSVidVideoRenderer.get_UsingOverlay
title: IMSVidVideoRenderer::get_UsingOverlay
author: windows-sdk-content
description: The get_UsingOverlay method queries whether the Video Mixing Renderer (VMR) is using the hardware overlay.
old-location: mstv\imsvidvideorenderer_get_usingoverlay.htm
old-project: mstv
ms.assetid: bd41cbcc-b8a8-4b08-9b25-399e366614ce
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_UsingOverlay method, IMSVidVideoRenderer.get_UsingOverlay, IMSVidVideoRenderer::get_UsingOverlay, IMSVidVideoRendererget_UsingOverlay, get_UsingOverlay, get_UsingOverlay method [Microsoft TV Technologies], get_UsingOverlay method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_usingoverlay, segment/IMSVidVideoRenderer::get_UsingOverlay
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
-	IMSVidVideoRenderer.get_UsingOverlay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get_UsingOverlay


## -description


The <b>get_UsingOverlay</b> method queries whether the Video Mixing Renderer (VMR) is using the hardware overlay.


## -parameters




### -param UseOverlayVal






#### - pUseOverlayVal [out]

Receives one of the following values.
            

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The VMR is using the hardware overlay.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The VMR is not using the hardware overlay.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/ee7a5c92-bdae-4b67-9b2b-5fb4ae3a8fd7">IMSVidVideoRenderer::put_UsingOverlay</a>
 

 

