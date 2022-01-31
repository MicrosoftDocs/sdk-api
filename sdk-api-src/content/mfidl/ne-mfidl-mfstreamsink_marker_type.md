---
UID: NE:mfidl._MFSTREAMSINK_MARKER_TYPE
title: MFSTREAMSINK_MARKER_TYPE (mfidl.h)
description: Defines stream marker information for the IMFStreamSink::PlaceMarker method.
helpviewer_keywords: ["MFSTREAMSINK_MARKER_DEFAULT","MFSTREAMSINK_MARKER_ENDOFSEGMENT","MFSTREAMSINK_MARKER_EVENT","MFSTREAMSINK_MARKER_TICK","MFSTREAMSINK_MARKER_TYPE","MFSTREAMSINK_MARKER_TYPE enumeration [Media Foundation]","d1c5f8ee-a451-44af-bf43-7623cea2be37","enumeration [Media Foundation]","mf.mfstreamsink_marker_type","mfidl/MFSTREAMSINK_MARKER_DEFAULT","mfidl/MFSTREAMSINK_MARKER_ENDOFSEGMENT","mfidl/MFSTREAMSINK_MARKER_EVENT","mfidl/MFSTREAMSINK_MARKER_TICK","mfidl/MFSTREAMSINK_MARKER_TYPE"]
old-location: mf\mfstreamsink_marker_type.htm
tech.root: mf
ms.assetid: d1c5f8ee-a451-44af-bf43-7623cea2be37
ms.date: 12/05/2018
ms.keywords: MFSTREAMSINK_MARKER_DEFAULT, MFSTREAMSINK_MARKER_ENDOFSEGMENT, MFSTREAMSINK_MARKER_EVENT, MFSTREAMSINK_MARKER_TICK, MFSTREAMSINK_MARKER_TYPE, MFSTREAMSINK_MARKER_TYPE enumeration [Media Foundation], d1c5f8ee-a451-44af-bf43-7623cea2be37, enumeration [Media Foundation], mf.mfstreamsink_marker_type, mfidl/MFSTREAMSINK_MARKER_DEFAULT, mfidl/MFSTREAMSINK_MARKER_ENDOFSEGMENT, mfidl/MFSTREAMSINK_MARKER_EVENT, mfidl/MFSTREAMSINK_MARKER_TICK, mfidl/MFSTREAMSINK_MARKER_TYPE
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFSTREAMSINK_MARKER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFSTREAMSINK_MARKER_TYPE
 - mfidl/_MFSTREAMSINK_MARKER_TYPE
 - MFSTREAMSINK_MARKER_TYPE
 - mfidl/MFSTREAMSINK_MARKER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSTREAMSINK_MARKER_TYPE
---

# MFSTREAMSINK_MARKER_TYPE enumeration


## -description

Defines stream marker information for the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a> method. The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">PlaceMarker</a> method places a marker on the stream between samples. The <b>MFSTREAMSINK_MARKER_TYPE</b> enumeration defines the marker type and the type of information associated with the marker.

## -enum-fields

### -field MFSTREAMSINK_MARKER_DEFAULT:0

This marker is for the application's use and does not convey any information to the stream sink.

### -field MFSTREAMSINK_MARKER_ENDOFSEGMENT

This marker indicates the end of a segment within a presentation. There might be a gap in the stream until the next segment starts. There is no data associated with this marker.

### -field MFSTREAMSINK_MARKER_TICK

This marker indicates that there is a gap in the stream. The marker data is a <b>LONGLONG</b> value (VT_I8) that specifies the time for the missing sample. The next sample received after this marker might but will not necessarily have the discontinuity flag: the data might remain continuous after the time gap. This marker corresponds to an <a href="/windows/desktop/medfound/mestreamtick">MEStreamTick</a> event from the stream.

### -field MFSTREAMSINK_MARKER_EVENT

This marker contains a media event. The marker data is a pointer to the event's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface (VT_UNKNOWN).

## -remarks

If the <a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a> receives an <b>MFSTREAMSINK_MARKER_TICK</b> marker, it inserts silence to cover the gap in the data.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
