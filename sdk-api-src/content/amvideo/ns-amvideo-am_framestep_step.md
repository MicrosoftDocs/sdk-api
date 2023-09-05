---
UID: NS:amvideo._AM_FRAMESTEP_STEP
title: AM_FRAMESTEP_STEP (amvideo.h)
description: Specifies the number of frames to step.
helpviewer_keywords: ["AM_FRAMESTEP_STEP","AM_FRAMESTEP_STEP structure [DirectShow]","AM_PROPERTY_FRAMESTEPStructure","_AM_FRAMESTEP_STEP","amvideo/AM_FRAMESTEP_STEP","dshow.am_property_framestep"]
old-location: dshow\am_property_framestep.htm
tech.root: dshow
ms.assetid: 342029c8-0b2b-45d2-852d-062a8d297d28
ms.date: 4/26/2023
ms.keywords: AM_FRAMESTEP_STEP, AM_FRAMESTEP_STEP structure [DirectShow], AM_PROPERTY_FRAMESTEPStructure, _AM_FRAMESTEP_STEP, amvideo/AM_FRAMESTEP_STEP, dshow.am_property_framestep
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
req.typenames: AM_FRAMESTEP_STEP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_FRAMESTEP_STEP
 - amvideo/_AM_FRAMESTEP_STEP
 - AM_FRAMESTEP_STEP
 - amvideo/AM_FRAMESTEP_STEP
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
 - AM_FRAMESTEP_STEP
---

# AM_FRAMESTEP_STEP structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the number of frames to step.

## -struct-fields

### -field dwFramesToStep

<b>DWORD</b> value specifying to the decoder the number of frames to step. Must be at least 1. If greater than 1, this instruction means to skip <i>n</i> - 1 frames and show the <i>n</i>th.

## -see-also

<a href="/windows/desktop/DirectShow/frame-stepping-property-set">Frame Stepping Property Set</a>