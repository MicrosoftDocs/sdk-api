---
UID: NE:strmif.VMR_ASPECT_RATIO_MODE
title: VMR_ASPECT_RATIO_MODE (strmif.h)
description: The VMR_ASPECT_RATIO_MODE enumeration type describes whether the Video Mixing Renderer Filter 7 preserves the aspect ratio of the source video.
helpviewer_keywords: ["VMR_ARMODE_LETTER_BOX","VMR_ARMODE_NONE","VMR_ASPECT_RATIO_MODE","VMR_ASPECT_RATIO_MODE","VMR_ASPECT_RATIO_MODE enumeration [DirectShow]","VMR_ASPECT_RATIO_MODEEnumeration","dshow.vmr_aspect_ratio_mode","strmif/VMR_ARMODE_LETTER_BOX","strmif/VMR_ARMODE_NONE","strmif/VMR_ASPECT_RATIO_MODE"]
old-location: dshow\vmr_aspect_ratio_mode.htm
tech.root: dshow
ms.assetid: dd1d1d99-008b-4234-a38a-314ba02bb116
ms.date: 4/26/2023
ms.keywords: VMR_ARMODE_LETTER_BOX, VMR_ARMODE_NONE, VMR_ASPECT_RATIO_MODE, VMR_ASPECT_RATIO_MODE , VMR_ASPECT_RATIO_MODE enumeration [DirectShow], VMR_ASPECT_RATIO_MODEEnumeration, dshow.vmr_aspect_ratio_mode, strmif/VMR_ARMODE_LETTER_BOX, strmif/VMR_ARMODE_NONE, strmif/VMR_ASPECT_RATIO_MODE
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
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
req.typenames: VMR_ASPECT_RATIO_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VMR_ASPECT_RATIO_MODE
 - strmif/VMR_ASPECT_RATIO_MODE
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
 - VMR_ASPECT_RATIO_MODE
---

# VMR_ASPECT_RATIO_MODE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VMR_ASPECT_RATIO_MODE</b> enumeration type describes whether the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> preserves the aspect ratio of the source video.

## -enum-fields

### -field VMR_ARMODE_NONE:0

Indicates that the VMR will not try to maintain the aspect ratio of the source video.

### -field VMR_ARMODE_LETTER_BOX

Indicates that the VMR will maintain the aspect ratio of the source video by letterboxing within the output rectangle.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmraspectratiocontrol">IVMRAspectRatioControl Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>
