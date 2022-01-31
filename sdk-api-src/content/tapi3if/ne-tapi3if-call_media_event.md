---
UID: NE:tapi3if.CALL_MEDIA_EVENT
title: CALL_MEDIA_EVENT (tapi3if.h)
description: The CALL_MEDIA_EVENT enum describes call media events. The ITCallMediaEvent::get_Event method returns a member of this enum to indicate the type of call media event that occurred.
helpviewer_keywords: ["CALL_MEDIA_EVENT","CALL_MEDIA_EVENT enumeration [TAPI 2.2]","CME_NEW_STREAM","CME_STREAM_ACTIVE","CME_STREAM_FAIL","CME_STREAM_INACTIVE","CME_STREAM_NOT_USED","CME_TERMINAL_FAIL","_tapi3_call_media_event","tapi3.call_media_event","tapi3if/CALL_MEDIA_EVENT","tapi3if/CME_NEW_STREAM","tapi3if/CME_STREAM_ACTIVE","tapi3if/CME_STREAM_FAIL","tapi3if/CME_STREAM_INACTIVE","tapi3if/CME_STREAM_NOT_USED","tapi3if/CME_TERMINAL_FAIL"]
old-location: tapi3\call_media_event.htm
tech.root: tapi3
ms.assetid: 835759f4-652b-4d01-911a-e580bb29d292
ms.date: 12/05/2018
ms.keywords: CALL_MEDIA_EVENT, CALL_MEDIA_EVENT enumeration [TAPI 2.2], CME_NEW_STREAM, CME_STREAM_ACTIVE, CME_STREAM_FAIL, CME_STREAM_INACTIVE, CME_STREAM_NOT_USED, CME_TERMINAL_FAIL, _tapi3_call_media_event, tapi3.call_media_event, tapi3if/CALL_MEDIA_EVENT, tapi3if/CME_NEW_STREAM, tapi3if/CME_STREAM_ACTIVE, tapi3if/CME_STREAM_FAIL, tapi3if/CME_STREAM_INACTIVE, tapi3if/CME_STREAM_NOT_USED, tapi3if/CME_TERMINAL_FAIL
req.header: tapi3if.h
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
req.typenames: CALL_MEDIA_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALL_MEDIA_EVENT
 - tapi3if/CALL_MEDIA_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALL_MEDIA_EVENT
---

# CALL_MEDIA_EVENT enumeration


## -description

The 
<b>CALL_MEDIA_EVENT</b> enum describes call media events. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_event">ITCallMediaEvent::get_Event</a> method returns a member of this enum to indicate the type of call media event that occurred.

## -enum-fields

### -field CME_NEW_STREAM:0

A new media stream has been created.

### -field CME_STREAM_FAIL

A media stream or stream request has failed.

### -field CME_TERMINAL_FAIL

A terminal has failed.

### -field CME_STREAM_NOT_USED

The media stream has not been used.

### -field CME_STREAM_ACTIVE

The media stream is active.

### -field CME_STREAM_INACTIVE

The media stream is not active.

### -field CME_LASTITEM

## -remarks

Due to latency, stream events may continue for a few seconds after a stream or related call session has been torn down.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_event">ITCallMediaEvent::get_Event</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
