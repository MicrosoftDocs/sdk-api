---
UID: NS:vmr9._VMR9VideoDesc
title: VMR9VideoDesc (vmr9.h)
description: The VMR9VideoDesc structure describes a video stream to be deinterlaced.
helpviewer_keywords: ["VMR9VideoDesc","VMR9VideoDesc structure [DirectShow]","VMR9VideoDescStructure","dshow.vmr9videodesc","vmr9/VMR9VideoDesc"]
old-location: dshow\vmr9videodesc.htm
tech.root: dshow
ms.assetid: af4bf46a-fae7-4485-b5fb-3fd1857f383f
ms.date: 4/26/2023
ms.keywords: VMR9VideoDesc, VMR9VideoDesc structure [DirectShow], VMR9VideoDescStructure, dshow.vmr9videodesc, vmr9/VMR9VideoDesc
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
req.typenames: VMR9VideoDesc
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9VideoDesc
 - vmr9/_VMR9VideoDesc
 - VMR9VideoDesc
 - vmr9/VMR9VideoDesc
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
 - VMR9VideoDesc
---

# VMR9VideoDesc structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9VideoDesc</code> structure describes a video stream to be deinterlaced.

## -struct-fields

### -field dwSize

Size of the structure, in bytes.

### -field dwSampleWidth

Width of the video to be deinterlaced, in pixels.

### -field dwSampleHeight

Height of the video to be deinterlaced, in pixels.

### -field SampleFormat

Specifies the interlacing format of the sample, as a member of the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9_sampleformat">VMR9_SampleFormat</a> enumeration.

### -field dwFourCC

Specifies the FOURCC code. Valid values include NV12, YV12, YUY2, UYVY, IMC1, IMC2, IMC3 and IMC4

### -field InputSampleFreq

A <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9frequency">VMR9Frequency</a> structure that specifies the input frequency. For NTSC TV, the frequency would be expressed as 30,000:1001.

### -field OutputFrameFreq

A **VMRFrequency** structure that specifies the output frequency. For NTSC TV, the frequency would be expressed as 60,000:1001.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>