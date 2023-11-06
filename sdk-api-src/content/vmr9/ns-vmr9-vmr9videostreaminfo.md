---
UID: NS:vmr9._VMR9VideoStreamInfo
title: VMR9VideoStreamInfo (vmr9.h)
description: The VMR9VideoStreamInfo structure describes the rendering parameters for a video compositing operation in the VRM-9 filter. This structure is used in the IVMRImageCompositor9::CompositeImage method.
helpviewer_keywords: ["VMR9VideoStreamInfo","VMR9VideoStreamInfo structure [DirectShow]","VMR9VideoStreamInfoStructure","dshow.vmr9videostreaminfo","vmr9/VMR9VideoStreamInfo"]
old-location: dshow\vmr9videostreaminfo.htm
tech.root: dshow
ms.assetid: e2da0c1e-d592-49ce-937c-0d75ce270282
ms.date: 4/26/2023
ms.keywords: VMR9VideoStreamInfo, VMR9VideoStreamInfo structure [DirectShow], VMR9VideoStreamInfoStructure, dshow.vmr9videostreaminfo, vmr9/VMR9VideoStreamInfo
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
req.typenames: VMR9VideoStreamInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9VideoStreamInfo
 - vmr9/_VMR9VideoStreamInfo
 - VMR9VideoStreamInfo
 - vmr9/VMR9VideoStreamInfo
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
 - VMR9VideoStreamInfo
---

# VMR9VideoStreamInfo structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9VideoStreamInfo</code> structure describes the rendering parameters for a video compositing operation in the VRM-9 filter. This structure is used in the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrimagecompositor9-compositeimage">IVMRImageCompositor9::CompositeImage</a> method.

## -struct-fields

### -field pddsVideoSurface

A pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface of the Direct3D surface that contains the video to be composited.

### -field dwWidth

The width of the video rectangle.

### -field dwHeight

The height of the video rectangle.

### -field dwStrmID

Specifies the input stream. This value corresponds to the input pin.

### -field fAlpha

The alpha value for this stream. (Not per-pixel alpha.)

### -field rNormal

The position of the image in composition space, as a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9normalizedrect">VMR9NormalizedRect</a> structure.

### -field rtStart

The start time of the video frame, in 100-nanosecond units.

### -field rtEnd

The end time of the video frame, in 100-nanosecond units.

### -field SampleFormat

The video interlacing format, specified as a member of the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9_sampleformat">VMR9_SampleFormat</a> enumeration type.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>