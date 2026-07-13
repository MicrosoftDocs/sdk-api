---
UID: NS:strmif.REGPINTYPES
title: REGPINTYPES (strmif.h)
description: The REGPINTYPES structure contains media type information for registering a filter.
helpviewer_keywords: ["AMOVIESETUP_MEDIATYPE","AMOVIESETUP_MEDIATYPE structure [DirectShow]","LPAMOVIESETUP_MEDIATYPE","LPAMOVIESETUP_MEDIATYPE structure pointer [DirectShow]","PAMOVIESETUP_MEDIATYPE","PAMOVIESETUP_MEDIATYPE structure pointer [DirectShow]","REGPINTYPES","REGPINTYPES structure [DirectShow]","REGPINTYPESStructure","dshow.regpintypes","strmif/AMOVIESETUP_MEDIATYPE","strmif/LPAMOVIESETUP_MEDIATYPE","strmif/PAMOVIESETUP_MEDIATYPE","strmif/REGPINTYPES"]
old-location: dshow\regpintypes.htm
tech.root: dshow
ms.assetid: aa31f856-4151-420d-a69d-34ef3a105130
ms.date: 4/26/2023
ms.keywords: AMOVIESETUP_MEDIATYPE, AMOVIESETUP_MEDIATYPE structure [DirectShow], LPAMOVIESETUP_MEDIATYPE, LPAMOVIESETUP_MEDIATYPE structure pointer [DirectShow], PAMOVIESETUP_MEDIATYPE, PAMOVIESETUP_MEDIATYPE structure pointer [DirectShow], REGPINTYPES, REGPINTYPES structure [DirectShow], REGPINTYPESStructure, dshow.regpintypes, strmif/AMOVIESETUP_MEDIATYPE, strmif/LPAMOVIESETUP_MEDIATYPE, strmif/PAMOVIESETUP_MEDIATYPE, strmif/REGPINTYPES
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
req.typenames: REGPINTYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - REGPINTYPES
 - strmif/REGPINTYPES
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
 - REGPINTYPES
---

# REGPINTYPES structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>REGPINTYPES</code> structure contains media type information for registering a filter.

## -struct-fields

### -field clsMajorType

Major type GUID of the media type.

### -field clsMinorType

Sub type GUID of the media type. Can be MEDIASUBTYPE_NULL.

## -remarks

This structure is used by the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface to identify the media types that a pin supports. The equivalent <b>AMOVIESETUP_MEDIATYPE</b> type is used in class factory templates (<a href="/windows/desktop/DirectShow/cfactorytemplate">CFactoryTemplate</a>).

To register a range of subtypes within the same major type, use the value MEDIASUBTYPE_NULL.

For more information, see <a href="/windows/desktop/DirectShow/how-to-register-directshow-filters">How to Register DirectShow Filters</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/media-types">Media Types</a>