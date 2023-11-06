---
UID: NF:segment.IMSVidVideoRenderer.get_UsingOverlay
title: IMSVidVideoRenderer::get_UsingOverlay (segment.h)
description: The get_UsingOverlay method queries whether the Video Mixing Renderer (VMR) is using the hardware overlay.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_UsingOverlay method","IMSVidVideoRenderer.get_UsingOverlay","IMSVidVideoRenderer::get_UsingOverlay","IMSVidVideoRendererget_UsingOverlay","get_UsingOverlay","get_UsingOverlay method [Microsoft TV Technologies]","get_UsingOverlay method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_usingoverlay","segment/IMSVidVideoRenderer::get_UsingOverlay"]
old-location: mstv\imsvidvideorenderer_get_usingoverlay.htm
tech.root: mstv
ms.assetid: bd41cbcc-b8a8-4b08-9b25-399e366614ce
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_UsingOverlay method, IMSVidVideoRenderer.get_UsingOverlay, IMSVidVideoRenderer::get_UsingOverlay, IMSVidVideoRendererget_UsingOverlay, get_UsingOverlay, get_UsingOverlay method [Microsoft TV Technologies], get_UsingOverlay method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_usingoverlay, segment/IMSVidVideoRenderer::get_UsingOverlay
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidVideoRenderer::get_UsingOverlay
 - segment/IMSVidVideoRenderer::get_UsingOverlay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get_UsingOverlay
---

# IMSVidVideoRenderer::get_UsingOverlay


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_UsingOverlay</b> method queries whether the Video Mixing Renderer (VMR) is using the hardware overlay.

## -parameters

### -param UseOverlayVal [out]

Receives one of the following values.
            

<table>
<tr>
<th>Value
                </th>
<th>Description
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

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_usingoverlay">IMSVidVideoRenderer::put_UsingOverlay</a>