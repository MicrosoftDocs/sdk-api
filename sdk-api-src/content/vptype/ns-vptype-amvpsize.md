---
UID: NS:vptype._AMVPSIZE
title: AMVPSIZE (vptype.h)
description: The AMVPSIZE structure specifies the width and height for a VP image.
helpviewer_keywords: ["*LPAMVPSIZE","AMVPSIZE","AMVPSIZE structure [DirectShow]","AMVPSIZEStructure","LPAMVPSIZE","LPAMVPSIZE structure pointer [DirectShow]","dshow.amvpsize","vptype/AMVPSIZE","vptype/LPAMVPSIZE"]
old-location: dshow\amvpsize.htm
tech.root: dshow
ms.assetid: e36163bc-a7ea-421e-b876-2d459ecb11e8
ms.date: 4/26/2023
ms.keywords: '*LPAMVPSIZE, AMVPSIZE, AMVPSIZE structure [DirectShow], AMVPSIZEStructure, LPAMVPSIZE, LPAMVPSIZE structure pointer [DirectShow], dshow.amvpsize, vptype/AMVPSIZE, vptype/LPAMVPSIZE'
req.header: vptype.h
req.include-header: 
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMVPSIZE
 - vptype/_AMVPSIZE
 - LPAMVPSIZE
 - vptype/LPAMVPSIZE
 - AMVPSIZE
 - vptype/AMVPSIZE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVPSIZE
---

# AMVPSIZE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMVPSIZE</b> structure specifies the width and height for a VP image.

## -struct-fields

### -field dwWidth

Width, in pixels.

### -field dwHeight

Height.

## -remarks

The context could be anything such as scaling, cropping, and so on.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>