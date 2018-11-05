---
UID: NE:mfidl._MFSTREAMSINK_MARKER_TYPE
title: "_MFSTREAMSINK_MARKER_TYPE"
author: windows-sdk-content
description: Defines stream marker information for the IMFStreamSink::PlaceMarker method.
old-location: mf\mfstreamsink_marker_type.htm
tech.root: medfound
ms.assetid: d1c5f8ee-a451-44af-bf43-7623cea2be37
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFSTREAMSINK_MARKER_DEFAULT, MFSTREAMSINK_MARKER_ENDOFSEGMENT, MFSTREAMSINK_MARKER_EVENT, MFSTREAMSINK_MARKER_TICK, MFSTREAMSINK_MARKER_TYPE, MFSTREAMSINK_MARKER_TYPE enumeration [Media Foundation], _MFSTREAMSINK_MARKER_TYPE, d1c5f8ee-a451-44af-bf43-7623cea2be37, enumeration [Media Foundation], mf.mfstreamsink_marker_type, mfidl/MFSTREAMSINK_MARKER_DEFAULT, mfidl/MFSTREAMSINK_MARKER_ENDOFSEGMENT, mfidl/MFSTREAMSINK_MARKER_EVENT, mfidl/MFSTREAMSINK_MARKER_TICK, mfidl/MFSTREAMSINK_MARKER_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSTREAMSINK_MARKER_TYPE
product: Windows
targetos: Windows
req.typenames: MFSTREAMSINK_MARKER_TYPE
req.redist: 
---

# _MFSTREAMSINK_MARKER_TYPE enumeration


## -description


Defines stream marker information for the <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">IMFStreamSink::PlaceMarker</a> method. The <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">PlaceMarker</a> method places a marker on the stream between samples. The <b>MFSTREAMSINK_MARKER_TYPE</b> enumeration defines the marker type and the type of information associated with the marker.


## -enum-fields




### -field MFSTREAMSINK_MARKER_DEFAULT

This marker is for the application's use and does not convey any information to the stream sink.


### -field MFSTREAMSINK_MARKER_ENDOFSEGMENT

This marker indicates the end of a segment within a presentation. There might be a gap in the stream until the next segment starts. There is no data associated with this marker.


### -field MFSTREAMSINK_MARKER_TICK

This marker indicates that there is a gap in the stream. The marker data is a <b>LONGLONG</b> value (VT_I8) that specifies the time for the missing sample. The next sample received after this marker will have the discontinuity flag. This marker corresponds to an <a href="https://msdn.microsoft.com/1a00fff1-c3ab-4965-a663-3c15bb48ea98">MEStreamTick</a> event from the stream.


### -field MFSTREAMSINK_MARKER_EVENT

This marker contains a media event. The marker data is a pointer to the event's <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface (VT_UNKNOWN).


## -remarks



If the <a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a> receives an <b>MFSTREAMSINK_MARKER_TICK</b> marker, it inserts silence to cover the gap in the data. 




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

