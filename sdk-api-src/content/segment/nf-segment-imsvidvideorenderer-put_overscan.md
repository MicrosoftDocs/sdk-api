---
UID: NF:segment.IMSVidVideoRenderer.put_OverScan
title: IMSVidVideoRenderer::put_OverScan (segment.h)
description: The put_OverScan method specifies the amount of clipping to perform on all sides of the video frame to cut off random video noise.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_OverScan method","IMSVidVideoRenderer.put_OverScan","IMSVidVideoRenderer::put_OverScan","IMSVidVideoRendererput_OverScan","mstv.imsvidvideorenderer_put_overscan","put_OverScan","put_OverScan method [Microsoft TV Technologies]","put_OverScan method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_OverScan"]
old-location: mstv\imsvidvideorenderer_put_overscan.htm
tech.root: mstv
ms.assetid: 141df99b-4fc7-439c-953e-1fa1c544258e
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_OverScan method, IMSVidVideoRenderer.put_OverScan, IMSVidVideoRenderer::put_OverScan, IMSVidVideoRendererput_OverScan, mstv.imsvidvideorenderer_put_overscan, put_OverScan, put_OverScan method [Microsoft TV Technologies], put_OverScan method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_OverScan
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
 - IMSVidVideoRenderer::put_OverScan
 - segment/IMSVidVideoRenderer::put_OverScan
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
 - IMSVidVideoRenderer.put_OverScan
---

# IMSVidVideoRenderer::put_OverScan


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OverScan</b> method specifies the amount of clipping to perform on all sides of the video frame to cut off random video noise.

## -parameters

### -param lPercent [in]

Specifies the amount to clip, in hundredths of a percent. For example, 175 indicates 1.75%.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the current clipping mode is <b>sslClipByOverScan</b>, the VMR clips the video image by the specified amount. For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">IMSVidVideoRenderer::put_SourceSize</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_overscan">IMSVidVideoRenderer::get_OverScan</a>