---
UID: NS:amvideo.tag_TRUECOLORINFO
title: TRUECOLORINFO (amvideo.h)
description: The TRUECOLORINFO structure contains color palette and bitmask information for a video image.
helpviewer_keywords: ["TRUECOLORINFO","TRUECOLORINFO structure [DirectShow]","TRUECOLORINFOStructure","amvideo/TRUECOLORINFO","dshow.truecolorinfostructure"]
old-location: dshow\truecolorinfostructure.htm
tech.root: dshow
ms.assetid: 8269d8c2-ff8e-48e0-b4f6-06900a7ecfdc
ms.date: 4/26/2023
ms.keywords: TRUECOLORINFO, TRUECOLORINFO structure [DirectShow], TRUECOLORINFOStructure, amvideo/TRUECOLORINFO, dshow.truecolorinfostructure
req.header: amvideo.h
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
targetos: Windows
req.typenames: TRUECOLORINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_TRUECOLORINFO
 - amvideo/tag_TRUECOLORINFO
 - TRUECOLORINFO
 - amvideo/TRUECOLORINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - TRUECOLORINFO
---

# TRUECOLORINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>TRUECOLORINFO</b> structure contains color palette and bitmask information for a video image.

## -struct-fields

### -field dwBitMasks

Array of color masks (one per color element).

### -field bmiColors

Array of palette colors.

## -remarks

This structure is not used for some RGB formats. For more information about which fields are valid under different circumstances, see the Platform SDK documentation for <b>BITMAPINFO</b>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a>