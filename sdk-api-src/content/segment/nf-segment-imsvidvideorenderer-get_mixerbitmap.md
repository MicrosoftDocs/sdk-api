---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmap
title: IMSVidVideoRenderer::get_MixerBitmap (segment.h)
description: The get_MixerBitmap method retrieves the static bitmap image, as an IPictureDisp type.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_MixerBitmap method","IMSVidVideoRenderer.get_MixerBitmap","IMSVidVideoRenderer::get_MixerBitmap","IMSVidVideoRendererget_MixerBitmap","get_MixerBitmap","get_MixerBitmap method [Microsoft TV Technologies]","get_MixerBitmap method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_mixerbitmap","segment/IMSVidVideoRenderer::get_MixerBitmap"]
old-location: mstv\imsvidvideorenderer_get_mixerbitmap.htm
tech.root: mstv
ms.assetid: cfcfab14-7084-4716-8955-574168cd3506
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmap method, IMSVidVideoRenderer.get_MixerBitmap, IMSVidVideoRenderer::get_MixerBitmap, IMSVidVideoRendererget_MixerBitmap, get_MixerBitmap, get_MixerBitmap method [Microsoft TV Technologies], get_MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmap, segment/IMSVidVideoRenderer::get_MixerBitmap
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
 - IMSVidVideoRenderer::get_MixerBitmap
 - segment/IMSVidVideoRenderer::get_MixerBitmap
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
 - IMSVidVideoRenderer.get_MixerBitmap
---

# IMSVidVideoRenderer::get_MixerBitmap


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MixerBitmap</b> method retrieves the static bitmap image, as an <b>IPictureDisp</b> type.

## -parameters

### -param MixerPictureDisp [out]

Receives an <b>IPictureDisp</b> interface pointer. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
No bitmap was set.

</td>
</tr>
</table>

## -remarks

If the static bitmap image is set, the VMR alpha-blends the bitmap onto the video image. For information about the <b>IPictureDisp</b> interface, see the Platform SDK documentation.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmapopacity">IMSVidVideoRenderer::get_MixerBitmapOpacity</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmappositionrect">IMSVidVideoRenderer::get_MixerBitmapPositionRect</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmap">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="/previous-versions/windows/desktop/mstv/mixing-an-image-onto-the-video-window-in-c-">Mixing an Image Onto the Video Window in C++</a>