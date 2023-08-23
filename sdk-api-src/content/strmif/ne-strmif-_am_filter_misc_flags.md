---
UID: NE:strmif._AM_FILTER_MISC_FLAGS
title: "_AM_FILTER_MISC_FLAGS (strmif.h)"
description: The _AM_FILTER_MISC_FLAGS enumeration contains flags that indicate whether a filter is a source filter or a renderer filter.
helpviewer_keywords: ["AM_FILTER_MISC_FLAGSEnumeration","AM_FILTER_MISC_FLAGS_IS_RENDERER","AM_FILTER_MISC_FLAGS_IS_SOURCE","_AM_FILTER_MISC_FLAGS","_AM_FILTER_MISC_FLAGS enumeration [DirectShow]","dshow._am_filter_misc_flags","strmif/AM_FILTER_MISC_FLAGS_IS_RENDERER","strmif/AM_FILTER_MISC_FLAGS_IS_SOURCE","strmif/_AM_FILTER_MISC_FLAGS"]
old-location: dshow\_am_filter_misc_flags.htm
tech.root: dshow
ms.assetid: 7acc160c-0da8-4b85-b88c-82b59ec38106
ms.date: 4/26/2023
ms.keywords: AM_FILTER_MISC_FLAGSEnumeration, AM_FILTER_MISC_FLAGS_IS_RENDERER, AM_FILTER_MISC_FLAGS_IS_SOURCE, _AM_FILTER_MISC_FLAGS, _AM_FILTER_MISC_FLAGS enumeration [DirectShow], dshow._am_filter_misc_flags, strmif/AM_FILTER_MISC_FLAGS_IS_RENDERER, strmif/AM_FILTER_MISC_FLAGS_IS_SOURCE, strmif/_AM_FILTER_MISC_FLAGS
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_FILTER_MISC_FLAGS
 - strmif/_AM_FILTER_MISC_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - _AM_FILTER_MISC_FLAGS
---

# _AM_FILTER_MISC_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>_AM_FILTER_MISC_FLAGS</b> enumeration contains flags that indicate whether a filter is a source filter or a renderer filter.

## -enum-fields

### -field AM_FILTER_MISC_FLAGS_IS_RENDERER:0x1

The filter is a renderer and sends an <a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a> event at the end of the stream.

### -field AM_FILTER_MISC_FLAGS_IS_SOURCE:0x2

The filter is a source filter.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamfiltermiscflags-getmiscflags">IAMFilterMiscFlags::GetMiscFlags</a>
