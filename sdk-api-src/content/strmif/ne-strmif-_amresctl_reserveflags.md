---
UID: NE:strmif._AMRESCTL_RESERVEFLAGS
title: "_AMRESCTL_RESERVEFLAGS (strmif.h)"
description: Specifies whether to increment or decrement the number of resources currently being reserved.
helpviewer_keywords: ["AMRESCTL_RESERVEFLAGS","AMRESCTL_RESERVEFLAGSEnumeration","AMRESCTL_RESERVEFLAGS_RESERVE","AMRESCTL_RESERVEFLAGS_UNRESERVE","_AMRESCTL_RESERVEFLAGS","_AMRESCTL_RESERVEFLAGS enumeration [DirectShow]","dshow.amresctl_reserveflags","strmif/AMRESCTL_RESERVEFLAGS_RESERVE","strmif/AMRESCTL_RESERVEFLAGS_UNRESERVE","strmif/_AMRESCTL_RESERVEFLAGS"]
old-location: dshow\amresctl_reserveflags.htm
tech.root: dshow
ms.assetid: 528c4e2e-2045-45a1-b502-75e103745c93
ms.date: 4/26/2023
ms.keywords: AMRESCTL_RESERVEFLAGS, AMRESCTL_RESERVEFLAGSEnumeration, AMRESCTL_RESERVEFLAGS_RESERVE, AMRESCTL_RESERVEFLAGS_UNRESERVE, _AMRESCTL_RESERVEFLAGS, _AMRESCTL_RESERVEFLAGS enumeration [DirectShow], dshow.amresctl_reserveflags, strmif/AMRESCTL_RESERVEFLAGS_RESERVE, strmif/AMRESCTL_RESERVEFLAGS_UNRESERVE, strmif/_AMRESCTL_RESERVEFLAGS
req.header: strmif.h
req.include-header: DShow.h
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
 - _AMRESCTL_RESERVEFLAGS
 - strmif/_AMRESCTL_RESERVEFLAGS
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
 - _AMRESCTL_RESERVEFLAGS
---

# _AMRESCTL_RESERVEFLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether to increment or decrement the number of resources currently being reserved.

## -enum-fields

### -field AMRESCTL_RESERVEFLAGS_RESERVE:0

Increment the reserved resource count.

### -field AMRESCTL_RESERVEFLAGS_UNRESERVE:0x1

Decrement the reserved resource count.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
