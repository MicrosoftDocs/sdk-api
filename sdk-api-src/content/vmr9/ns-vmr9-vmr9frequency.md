---
UID: NS:vmr9._VMR9Frequency
title: VMR9Frequency (vmr9.h)
description: The VMR9Frequency structure describes the frequency of a video stream. Frequencies are described as ratios. For example, the NTSC frame rate of 29.97 fps is expressed as 30,000:1001.
helpviewer_keywords: ["VMR9Frequency","VMR9Frequency structure [DirectShow]","VMR9FrequencyStructure","dshow.vmr9frequency","vmr9/VMR9Frequency"]
old-location: dshow\vmr9frequency.htm
tech.root: dshow
ms.assetid: a2d19dcf-521e-4df0-8e28-5561f2617411
ms.date: 4/26/2023
ms.keywords: VMR9Frequency, VMR9Frequency structure [DirectShow], VMR9FrequencyStructure, dshow.vmr9frequency, vmr9/VMR9Frequency
req.header: vmr9.h
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
req.typenames: VMR9Frequency
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9Frequency
 - vmr9/_VMR9Frequency
 - VMR9Frequency
 - vmr9/VMR9Frequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9Frequency
---

# VMR9Frequency structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9Frequency</code> structure describes the frequency of a video stream. Frequencies are described as ratios. For example, the NTSC frame rate of 29.97 fps is expressed as 30,000:1001.

## -struct-fields

### -field dwNumerator

Numerator of the frequency ratio.

### -field dwDenominator

Denominator of the frequency ratio.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>