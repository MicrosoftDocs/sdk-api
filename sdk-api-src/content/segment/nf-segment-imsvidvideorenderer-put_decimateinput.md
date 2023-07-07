---
UID: NF:segment.IMSVidVideoRenderer.put_DecimateInput
title: IMSVidVideoRenderer::put_DecimateInput (segment.h)
description: The put_DecimateInput method specifies whether the Video Mixing Renderer (VMR) will decimate the video (that is, reduce the native video size) before processing it.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_DecimateInput method","IMSVidVideoRenderer.put_DecimateInput","IMSVidVideoRenderer::put_DecimateInput","IMSVidVideoRendererput_DecimateInput","mstv.imsvidvideorenderer_put_decimateinput","put_DecimateInput","put_DecimateInput method [Microsoft TV Technologies]","put_DecimateInput method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_DecimateInput"]
old-location: mstv\imsvidvideorenderer_put_decimateinput.htm
tech.root: mstv
ms.assetid: e048a572-3a96-4610-9266-0e97b5a09778
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_DecimateInput method, IMSVidVideoRenderer.put_DecimateInput, IMSVidVideoRenderer::put_DecimateInput, IMSVidVideoRendererput_DecimateInput, mstv.imsvidvideorenderer_put_decimateinput, put_DecimateInput, put_DecimateInput method [Microsoft TV Technologies], put_DecimateInput method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_DecimateInput
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
 - IMSVidVideoRenderer::put_DecimateInput
 - segment/IMSVidVideoRenderer::put_DecimateInput
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
 - IMSVidVideoRenderer.put_DecimateInput
---

# IMSVidVideoRenderer::put_DecimateInput


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_DecimateInput</b> method specifies whether the Video Mixing Renderer (VMR) will decimate the video (that is, reduce the native video size) before processing it.

This method is currently not supported.

## -parameters

### -param pDeci

Specifies whether to enable or disable video decimation. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Enable video decimation.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable video decimation.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This property should be set to true when the native video stream is HDTV but the system monitor is set to a lower resolution. This prevents the VMR from doing unnecessary work by processing the video at high resolution and then shrinking it.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-setoutputrect">IVMRMixerControl::SetMixingPrefs</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>