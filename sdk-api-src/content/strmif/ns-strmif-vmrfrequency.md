---
UID: NS:strmif._VMRFrequency
title: VMRFrequency (strmif.h)
description: The VMRFrequency structure describes the frequency of a video stream. Frequencies are described as ratios. For example, the NTSC frame rate of 29.97 fps is expressed as 30,000:1001.
helpviewer_keywords: ["VMRFrequency","VMRFrequency structure [DirectShow]","VMRFrequencyStructure","dshow.vmrfrequency","strmif/VMRFrequency"]
old-location: dshow\vmrfrequency.htm
tech.root: dshow
ms.assetid: fb4c094a-2760-45b2-b494-a44d5493987f
ms.date: 4/26/2023
ms.keywords: VMRFrequency, VMRFrequency structure [DirectShow], VMRFrequencyStructure, dshow.vmrfrequency, strmif/VMRFrequency
req.header: strmif.h
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
req.typenames: VMRFrequency
req.redist: 
req.product: Windows XP with SP1 and later
ms.custom: 19H1
f1_keywords:
 - _VMRFrequency
 - strmif/_VMRFrequency
 - VMRFrequency
 - strmif/VMRFrequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRFrequency
---

# VMRFrequency structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMRFrequency</code> structure describes the frequency of a video stream. Frequencies are described as ratios. For example, the NTSC frame rate of 29.97 fps is expressed as 30,000:1001.

## -struct-fields

### -field dwNumerator

Numerator of the frequency ratio.

### -field dwDenominator

Denominator of the frequency ratio.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>