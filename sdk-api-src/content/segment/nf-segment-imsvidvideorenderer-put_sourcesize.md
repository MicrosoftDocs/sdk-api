---
UID: NF:segment.IMSVidVideoRenderer.put_SourceSize
title: IMSVidVideoRenderer::put_SourceSize (segment.h)
description: The put_SourceSize method specifies the type of clipping to apply to the video rectangle, if any.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_SourceSize method","IMSVidVideoRenderer.put_SourceSize","IMSVidVideoRenderer::put_SourceSize","IMSVidVideoRendererput_SourceSize","mstv.imsvidvideorenderer_put_sourcesize","put_SourceSize","put_SourceSize method [Microsoft TV Technologies]","put_SourceSize method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_SourceSize"]
old-location: mstv\imsvidvideorenderer_put_sourcesize.htm
tech.root: mstv
ms.assetid: c792f064-a137-4872-8c79-6e924b6023f0
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_SourceSize method, IMSVidVideoRenderer.put_SourceSize, IMSVidVideoRenderer::put_SourceSize, IMSVidVideoRendererput_SourceSize, mstv.imsvidvideorenderer_put_sourcesize, put_SourceSize, put_SourceSize method [Microsoft TV Technologies], put_SourceSize method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_SourceSize
f1_keywords:
- segment/IMSVidVideoRenderer.put_SourceSize
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
- IMSVidVideoRenderer.put_SourceSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer::put_SourceSize


## -description


The <b>put_SourceSize</b> method specifies the type of clipping to apply to the video rectangle, if any.


## -parameters




### -param NewSize [in]

Specifies a member of the <a href="https://docs.microsoft.com/windows/desktop/api/segment/ne-segment-sourcesizelist">SourceSizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_sourcesize">IMSVidVideoRenderer::get_SourceSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_clippedsourcerect">IMSVidVideoRenderer::put_ClippedSourceRect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_overscan">IMSVidVideoRenderer::put_OverScan</a>
 

 

