---
UID: NF:segment.IMSVidVideoRenderer.put_UsingOverlay
title: IMSVidVideoRenderer::put_UsingOverlay (segment.h)
description: The put_UsingOverlay method specifies whether the Video Mixing Renderer will use the hardware overlay.helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_UsingOverlay method","IMSVidVideoRenderer.put_UsingOverlay","IMSVidVideoRenderer::put_UsingOverlay","IMSVidVideoRendererput_UsingOverlay","mstv.imsvidvideorenderer_put_usingoverlay","put_UsingOverlay","put_UsingOverlay method [Microsoft TV Technologies]","put_UsingOverlay method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_UsingOverlay"]
old-location: mstv\imsvidvideorenderer_put_usingoverlay.htm
tech.root: mstv
ms.assetid: ee7a5c92-bdae-4b67-9b2b-5fb4ae3a8fd7
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_UsingOverlay method, IMSVidVideoRenderer.put_UsingOverlay, IMSVidVideoRenderer::put_UsingOverlay, IMSVidVideoRendererput_UsingOverlay, mstv.imsvidvideorenderer_put_usingoverlay, put_UsingOverlay, put_UsingOverlay method [Microsoft TV Technologies], put_UsingOverlay method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_UsingOverlay
f1_keywords:
- segment/IMSVidVideoRenderer.put_UsingOverlay
dev_langs:
- c++
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
- IMSVidVideoRenderer.put_UsingOverlay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer::put_UsingOverlay


## -description


The <b>put_UsingOverlay</b> method specifies whether the Video Mixing Renderer will use the hardware overlay.


## -parameters




### -param UseOverlayVal [in]

Flag that specifies whether to use the hardware overlay. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Use the hardware overlay.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Do not use the hardware overlay.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_usingoverlay">IMSVidVideoRenderer::get_UsingOverlay</a>
 

 

