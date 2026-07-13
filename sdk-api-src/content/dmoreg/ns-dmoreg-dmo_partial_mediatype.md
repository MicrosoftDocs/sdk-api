---
UID: NS:dmoreg._DMO_PARTIAL_MEDIATYPE
title: DMO_PARTIAL_MEDIATYPE (dmoreg.h)
description: The DMO_PARTIAL_MEDIATYPE structure partially describes a media type used by a Microsoft DirectX Media Object (DMO). The DMO registration functions use this structure to specify supported media types.
helpviewer_keywords: ["*PDMO_PARTIAL_MEDIATYPE","DMO_PARTIAL_MEDIATYPE","DMO_PARTIAL_MEDIATYPE structure [DirectShow]","DMO_PARTIAL_MEDIATYPEStructure","PDMO_PARTIAL_MEDIATYPE","PDMO_PARTIAL_MEDIATYPE structure pointer [DirectShow]","dmoreg/DMO_PARTIAL_MEDIATYPE","dmoreg/PDMO_PARTIAL_MEDIATYPE","dshow.dmo_partial_mediatype"]
old-location: dshow\dmo_partial_mediatype.htm
tech.root: dshow
ms.assetid: 53bf4c34-d180-4edd-b59a-55d7d90708b5
ms.date: 4/26/2023
ms.keywords: '*PDMO_PARTIAL_MEDIATYPE, DMO_PARTIAL_MEDIATYPE, DMO_PARTIAL_MEDIATYPE structure [DirectShow], DMO_PARTIAL_MEDIATYPEStructure, PDMO_PARTIAL_MEDIATYPE, PDMO_PARTIAL_MEDIATYPE structure pointer [DirectShow], dmoreg/DMO_PARTIAL_MEDIATYPE, dmoreg/PDMO_PARTIAL_MEDIATYPE, dshow.dmo_partial_mediatype'
req.header: dmoreg.h
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
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DMO_PARTIAL_MEDIATYPE
 - dmoreg/_DMO_PARTIAL_MEDIATYPE
 - PDMO_PARTIAL_MEDIATYPE
 - dmoreg/PDMO_PARTIAL_MEDIATYPE
 - DMO_PARTIAL_MEDIATYPE
 - dmoreg/DMO_PARTIAL_MEDIATYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dmoreg.h
api_name:
 - DMO_PARTIAL_MEDIATYPE
---

# DMO_PARTIAL_MEDIATYPE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DMO_PARTIAL_MEDIATYPE</code> structure partially describes a media type used by a Microsoft DirectX Media Object (DMO). The DMO registration functions use this structure to specify supported media types.

## -struct-fields

### -field type

Major type GUID. Use GUID_NULL to match any major type.

### -field subtype

Subtype GUID. Use GUID_NULL to match any subtype.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-structures">DMO Structures</a>