---
UID: NS:amva._tag_AMVABeginFrameInfo
title: AMVABeginFrameInfo (amva.h)
description: The AMVABeginFrameInfo structure contains information for the IAMVideoAccelerator::BeginFrame method.
helpviewer_keywords: ["*LPAMVABeginFrameInfo","AMVABeginFrameInfo","AMVABeginFrameInfo structure [DirectShow]","AMVABeginFrameInfoStructure","LPAMVABeginFrameInfo","LPAMVABeginFrameInfo structure pointer [DirectShow]","amva/AMVABeginFrameInfo","amva/LPAMVABeginFrameInfo","dshow.amvabeginframeinfo"]
old-location: dshow\amvabeginframeinfo.htm
tech.root: dshow
ms.assetid: 49af9094-86d5-4c11-b871-41f9984e0faf
ms.date: 4/26/2023
ms.keywords: '*LPAMVABeginFrameInfo, AMVABeginFrameInfo, AMVABeginFrameInfo structure [DirectShow], AMVABeginFrameInfoStructure, LPAMVABeginFrameInfo, LPAMVABeginFrameInfo structure pointer [DirectShow], amva/AMVABeginFrameInfo, amva/LPAMVABeginFrameInfo, dshow.amvabeginframeinfo'
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
req.typenames: AMVABeginFrameInfo, *LPAMVABeginFrameInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVABeginFrameInfo
 - amva/_tag_AMVABeginFrameInfo
 - LPAMVABeginFrameInfo
 - amva/LPAMVABeginFrameInfo
 - AMVABeginFrameInfo
 - amva/AMVABeginFrameInfo
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
 - AMVABeginFrameInfo
---

# AMVABeginFrameInfo structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMVABeginFrameInfo</b> structure contains information for the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a> method.

## -struct-fields

### -field dwDestSurfaceIndex

The zero-based index of the uncompressed destination surface. The number of uncompressed surfaces is specified in the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo">IAMVideoAcceleratorNotify::SetUncompSurfacesInfo</a> method.

### -field pInputData

Pointer to a buffer that contains data for the video accelerator.

This buffer must contain a <b>WORD</b> value that is equal to the value of <b>dwDestSurfaceIndex</b>.

### -field dwSizeInputData

Size, in bytes, of the buffer that <b>pInputData</b> points to. The value must be 2.

### -field pOutputData

Pointer to a buffer that the video accelerator can write to.

This member must be <b>NULL</b>.

### -field dwSizeOutputData

Size, in bytes, of the buffer that <b>pOutputData</b> points to. The value must be zero.

## -remarks

The buffer pointed to by <b>pInputData</b> cannot contain pointer values, because their addresses will not be valid in kernel mode, where frame processing occurs.
      

The video accelerator might not use the same surface memory in two consecutive calls with the same frame index.
      Therefore, the decoder should not make any assumption about the initial contents of the frame.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a>