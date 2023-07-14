---
UID: NF:segment.IMSVidVideoRenderer.get_SourceSize
title: IMSVidVideoRenderer::get_SourceSize (segment.h)
description: The get_SourceSize method retrieves the type of clipping to apply to the video rectangle, if any.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_SourceSize method","IMSVidVideoRenderer.get_SourceSize","IMSVidVideoRenderer::get_SourceSize","IMSVidVideoRendererget_SourceSize","get_SourceSize","get_SourceSize method [Microsoft TV Technologies]","get_SourceSize method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_sourcesize","segment/IMSVidVideoRenderer::get_SourceSize"]
old-location: mstv\imsvidvideorenderer_get_sourcesize.htm
tech.root: mstv
ms.assetid: 312a2c1e-5332-4a2d-ada9-1dc8236f4170
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_SourceSize method, IMSVidVideoRenderer.get_SourceSize, IMSVidVideoRenderer::get_SourceSize, IMSVidVideoRendererget_SourceSize, get_SourceSize, get_SourceSize method [Microsoft TV Technologies], get_SourceSize method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_sourcesize, segment/IMSVidVideoRenderer::get_SourceSize
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
 - IMSVidVideoRenderer::get_SourceSize
 - segment/IMSVidVideoRenderer::get_SourceSize
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
 - IMSVidVideoRenderer.get_SourceSize
---

# IMSVidVideoRenderer::get_SourceSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SourceSize</b> method retrieves the type of clipping to apply to the video rectangle, if any.

## -parameters

### -param CurrentSize

Receives a member of the <a href="/windows/desktop/api/segment/ne-segment-sourcesizelist">SourceSizeList</a> enumeration.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">IMSVidVideoRenderer::put_SourceSize</a>