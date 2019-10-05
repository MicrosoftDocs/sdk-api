---
UID: NE:segment.SourceSizeList
title: SourceSizeList (segment.h)
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\sourcesizelist.htm
tech.root: mstv
ms.assetid: 579c4993-6238-47c7-b61c-398568c1fb94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MSVidCtlSourceSizeListEnumeration, SourceSizeList, SourceSizeList enumeration [Microsoft TV Technologies], enumeration [Microsoft TV Technologies], mstv.sourcesizelist, segment/SourceSizeList, segment/sslClipByClipRect, segment/sslClipByOverScan, segment/sslFullSize, sslClipByClipRect, sslClipByOverScan, sslFullSize
ms.topic: enum
f1_keywords: 
 - "segment/SourceSizeList"
dev_langs:
 - c++
req.header: segment.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - segment.h
api_name:
 - SourceSizeList
targetos: Windows
req.typenames: SourceSizeList
req.redist: 
ms.custom: 19H1
---

# SourceSizeList enumeration


## -description



This topic applies to Windows XP or later.
        



The <b>SourceSizeList</b> enumeration is used to indicate how the VMR will clip the source video rectangle.


## -enum-fields




### -field sslFullSize

Do not clip the source video rectangle.


### -field sslClipByOverScan

Clip the source video rectangle by the value specified in the last call to <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_overscan">IMSVidVideoRenderer::put_OverScan</a>.


### -field sslClipByClipRect

Clip the source video rectangle by the value specified in the last call to <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_clippedsourcerect">IMSVidVideoRenderer::put_ClippedSourceRect</a>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_sourcesize">IMSVidVideoRenderer::get_SourceSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">IMSVidVideoRenderer::put_SourceSize</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-enumerations">Video Control Enumerations</a>
 

 

