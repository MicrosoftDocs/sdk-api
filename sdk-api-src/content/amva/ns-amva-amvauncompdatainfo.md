---
UID: NS:amva._tag_AMVAUncompDataInfo
title: AMVAUncompDataInfo (amva.h)
description: The AMVAUncompDataInfo structure specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.
helpviewer_keywords: ["*LPAMVAUncompDataInfo","AMVAUncompDataInfo","AMVAUncompDataInfo structure [DirectShow]","AMVAUncompDataInfoStructure","LPAMVAUncompDataInfo","LPAMVAUncompDataInfo structure pointer [DirectShow]","amva/AMVAUncompDataInfo","amva/LPAMVAUncompDataInfo","dshow.amvauncompdatainfo"]
old-location: dshow\amvauncompdatainfo.htm
tech.root: dshow
ms.assetid: 920f88bb-c671-4ab9-b482-b03505cca118
ms.date: 4/26/2023
ms.keywords: '*LPAMVAUncompDataInfo, AMVAUncompDataInfo, AMVAUncompDataInfo structure [DirectShow], AMVAUncompDataInfoStructure, LPAMVAUncompDataInfo, LPAMVAUncompDataInfo structure pointer [DirectShow], amva/AMVAUncompDataInfo, amva/LPAMVAUncompDataInfo, dshow.amvauncompdatainfo'
req.header: amva.h
req.include-header: Videoacc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVAUncompDataInfo
 - amva/_tag_AMVAUncompDataInfo
 - LPAMVAUncompDataInfo
 - amva/LPAMVAUncompDataInfo
 - AMVAUncompDataInfo
 - amva/AMVAUncompDataInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amva.h
api_name:
 - AMVAUncompDataInfo
---

# AMVAUncompDataInfo structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMVAUncompDataInfo</b> structure specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.

## -struct-fields

### -field dwUncompWidth

Width of the decoded, uncompressed data, in pixels.

### -field dwUncompHeight

Height of the decoded, uncompressed data, in pixels.

### -field ddUncompPixelFormat

A <b>DDPIXELFORMAT</b> structure that specifies the pixel format of the uncompressed data.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo">IAMVideoAccelerator::GetCompBufferInfo</a>