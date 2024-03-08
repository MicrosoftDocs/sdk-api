---
UID: NS:strmif._VMRDeinterlaceCaps
title: VMRDeinterlaceCaps (strmif.h)
description: The VMRDeinterlaceCaps structure describes the capabilities of a deinterlacing mode.
helpviewer_keywords: ["VMRDeinterlaceCaps","VMRDeinterlaceCaps structure [DirectShow]","VMRDeinterlaceCapsStructure","dshow.vmrdeinterlacecaps","strmif/VMRDeinterlaceCaps"]
old-location: dshow\vmrdeinterlacecaps.htm
tech.root: dshow
ms.assetid: e6152130-d574-4c9e-9d35-a42de709f9ae
ms.date: 4/26/2023
ms.keywords: VMRDeinterlaceCaps, VMRDeinterlaceCaps structure [DirectShow], VMRDeinterlaceCapsStructure, dshow.vmrdeinterlacecaps, strmif/VMRDeinterlaceCaps
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
req.typenames: VMRDeinterlaceCaps
req.redist: 
req.product: Windows XP with SP1 and later
ms.custom: 19H1
f1_keywords:
 - _VMRDeinterlaceCaps
 - strmif/_VMRDeinterlaceCaps
 - VMRDeinterlaceCaps
 - strmif/VMRDeinterlaceCaps
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
 - VMRDeinterlaceCaps
---

# VMRDeinterlaceCaps structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMRDeinterlaceCaps</code> structure describes the capabilities of a deinterlacing mode.

## -struct-fields

### -field dwSize

Size of the structure, in bytes.

### -field dwNumPreviousOutputFrames

Number of previously de-interlaced frames that must be fed back to the hardware to deinterlace the next field. (Used by recursive deinterlacing algorithms.)

### -field dwNumForwardRefSamples

Number of future samples needed to deinterlace the current field.

### -field dwNumBackwardRefSamples

Number of past samples needed to deinterlace the current field.

### -field DeinterlaceTechnology

Bitwise combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-vmrdeinterlacetech">VMRDeinterlaceTech</a> enumeration type. These flags are used to describe the deinterlacing algorithm.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>