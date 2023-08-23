---
UID: NS:strmif.REGFILTERPINS2
title: REGFILTERPINS2 (strmif.h)
description: The REGFILTERPINS2 structure contains information for registering a filter through the IFilterMapper2 interface.
helpviewer_keywords: ["REGFILTERPINS2","REGFILTERPINS2 structure [DirectShow]","REGFILTERPINS2Structure","dshow.regfilterpins2","strmif/REGFILTERPINS2"]
old-location: dshow\regfilterpins2.htm
tech.root: dshow
ms.assetid: a78327f1-a0aa-4e25-b6f8-cf45b92191fa
ms.date: 4/26/2023
ms.keywords: REGFILTERPINS2, REGFILTERPINS2 structure [DirectShow], REGFILTERPINS2Structure, dshow.regfilterpins2, strmif/REGFILTERPINS2
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
req.typenames: REGFILTERPINS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - REGFILTERPINS2
 - strmif/REGFILTERPINS2
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
 - REGFILTERPINS2
---

# REGFILTERPINS2 structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>REGFILTERPINS2</code> structure contains information for registering a filter through the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface.

## -struct-fields

### -field dwFlags

Bitwise combination of zero or more <a href="/previous-versions/windows/desktop/legacy/dd377518(v=vs.85)">REG_PINFLAG</a> flags.

### -field cInstances

Number of instances of this pin.

### -field nMediaTypes

Number of media types supported by this pin.

### -field lpMediaType

Pointer to an array of <a href="/windows/desktop/api/strmif/ns-strmif-regpintypes">REGPINTYPES</a> structures, of size nMediaTypes.

### -field nMediums

Number of mediums. Can be zero.

### -field lpMedium

Pointer to an array of <a href="/windows/desktop/api/strmif/ns-strmif-regpinmedium">REGPINMEDIUM</a> structures, of size nMediums.

### -field clsPinCategory

Optional pin category, from the <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>.

## -remarks

If you use this structure, set the <b>dwVersion</b> member of the <a href="/windows/desktop/api/strmif/ns-strmif-regfilter2">REGFILTER2</a> structure to 2.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>