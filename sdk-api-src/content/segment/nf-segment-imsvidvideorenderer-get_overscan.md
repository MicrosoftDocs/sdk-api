---
UID: NF:segment.IMSVidVideoRenderer.get_OverScan
title: IMSVidVideoRenderer::get_OverScan (segment.h)
description: The get_OverScan method retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_OverScan method","IMSVidVideoRenderer.get_OverScan","IMSVidVideoRenderer::get_OverScan","IMSVidVideoRendererget_OverScan","get_OverScan","get_OverScan method [Microsoft TV Technologies]","get_OverScan method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_overscan","segment/IMSVidVideoRenderer::get_OverScan"]
old-location: mstv\imsvidvideorenderer_get_overscan.htm
tech.root: mstv
ms.assetid: 2c4946e6-b25c-4e6a-b640-73982c0da871
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_OverScan method, IMSVidVideoRenderer.get_OverScan, IMSVidVideoRenderer::get_OverScan, IMSVidVideoRendererget_OverScan, get_OverScan, get_OverScan method [Microsoft TV Technologies], get_OverScan method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_overscan, segment/IMSVidVideoRenderer::get_OverScan
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
 - IMSVidVideoRenderer::get_OverScan
 - segment/IMSVidVideoRenderer::get_OverScan
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
 - IMSVidVideoRenderer.get_OverScan
---

# IMSVidVideoRenderer::get_OverScan


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OverScan</b> method retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

## -parameters

### -param plPercent [out]

Receives the amount to clip, in hundredths of a percent.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the current clipping mode is <b>sslClipByOverScan</b>, the VMR clips the video image by the amount given in the <i>plPercent</i> parameter. For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">IMSVidVideoRenderer::put_SourceSize</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_overscan">IMSVidVideoRenderer::put_OverScan</a>