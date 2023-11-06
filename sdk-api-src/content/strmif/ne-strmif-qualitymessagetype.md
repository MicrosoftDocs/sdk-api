---
UID: NE:strmif.tagQualityMessageType
title: QualityMessageType (strmif.h)
description: Describes a quality message type.
helpviewer_keywords: ["Famine","Flood","QualityMessageType","QualityMessageType enumeration [DirectShow]","QualityMessageTypeEnumeration","dshow.qualitymessagetype","strmif/Famine","strmif/Flood","strmif/QualityMessageType"]
old-location: dshow\qualitymessagetype.htm
tech.root: dshow
ms.assetid: 54a2239d-bf37-499d-b8c4-f797c1b46933
ms.date: 4/26/2023
ms.keywords: Famine, Flood, QualityMessageType, QualityMessageType enumeration [DirectShow], QualityMessageTypeEnumeration, dshow.qualitymessagetype, strmif/Famine, strmif/Flood, strmif/QualityMessageType
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
req.typenames: QualityMessageType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQualityMessageType
 - strmif/tagQualityMessageType
 - QualityMessageType
 - strmif/QualityMessageType
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
 - QualityMessageType
---

# QualityMessageType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Describes a quality message type.

## -enum-fields

### -field Famine:0

Downstream filter needs more data.

### -field Flood

Downstream filter needs less data.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
