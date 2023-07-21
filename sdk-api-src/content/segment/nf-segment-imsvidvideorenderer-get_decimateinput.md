---
UID: NF:segment.IMSVidVideoRenderer.get_DecimateInput
title: IMSVidVideoRenderer::get_DecimateInput (segment.h)
description: The get_DecimateInput method queries whether the Video Mixing Renderer (VMR) is currently configured to decimate the video (that is, reduce the native video size) before processing it.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_DecimateInput method","IMSVidVideoRenderer.get_DecimateInput","IMSVidVideoRenderer::get_DecimateInput","IMSVidVideoRendererget_DecimateInput","get_DecimateInput","get_DecimateInput method [Microsoft TV Technologies]","get_DecimateInput method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_decimateinput","segment/IMSVidVideoRenderer::get_DecimateInput"]
old-location: mstv\imsvidvideorenderer_get_decimateinput.htm
tech.root: mstv
ms.assetid: 1f533b85-175b-4381-b7a9-eac0d8e313ed
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_DecimateInput method, IMSVidVideoRenderer.get_DecimateInput, IMSVidVideoRenderer::get_DecimateInput, IMSVidVideoRendererget_DecimateInput, get_DecimateInput, get_DecimateInput method [Microsoft TV Technologies], get_DecimateInput method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_decimateinput, segment/IMSVidVideoRenderer::get_DecimateInput
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
 - IMSVidVideoRenderer::get_DecimateInput
 - segment/IMSVidVideoRenderer::get_DecimateInput
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
 - IMSVidVideoRenderer.get_DecimateInput
---

# IMSVidVideoRenderer::get_DecimateInput


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_DecimateInput</b> method queries whether the Video Mixing Renderer (VMR) is currently configured to decimate the video (that is, reduce the native video size) before processing it.

This method is currently not supported.

## -parameters

### -param pDeci [out]

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
<td>The VMR is configured to decimate the video.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The VMR is not configured to decimate the video.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This property should be set to true when the native video stream is HDTV but the system monitor is set to a lower resolution. This prevents the VMR from doing unnecessary work by processing the video at high resolution and then shrinking it.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-getmixingprefs">IVMRMixerControl::GetMixingPrefs</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>