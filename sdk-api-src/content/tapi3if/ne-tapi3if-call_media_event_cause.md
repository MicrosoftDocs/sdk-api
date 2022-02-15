---
UID: NE:tapi3if.CALL_MEDIA_EVENT_CAUSE
title: CALL_MEDIA_EVENT_CAUSE (tapi3if.h)
description: The CALL_MEDIA_EVENT_CAUSE enum is used by ITCallMediaEvent::get_Cause method to return a description of what caused a media event, such as a device timeout.
helpviewer_keywords: ["CALL_MEDIA_EVENT_CAUSE","CALL_MEDIA_EVENT_CAUSE enumeration [TAPI 2.2]","CMC_BAD_DEVICE","CMC_CONNECT_FAIL","CMC_LOCAL_REQUEST","CMC_MEDIA_RECOVERED","CMC_MEDIA_TIMEOUT","CMC_REMOTE_REQUEST","CMC_UNKNOWN","_tapi3_call_media_event_cause","tapi3.call_media_event_cause","tapi3if/CALL_MEDIA_EVENT_CAUSE","tapi3if/CMC_BAD_DEVICE","tapi3if/CMC_CONNECT_FAIL","tapi3if/CMC_LOCAL_REQUEST","tapi3if/CMC_MEDIA_RECOVERED","tapi3if/CMC_MEDIA_TIMEOUT","tapi3if/CMC_REMOTE_REQUEST","tapi3if/CMC_UNKNOWN"]
old-location: tapi3\call_media_event_cause.htm
tech.root: tapi3
ms.assetid: c43e0a72-decc-47e3-bd5e-d94a95a2e404
ms.date: 12/05/2018
ms.keywords: CALL_MEDIA_EVENT_CAUSE, CALL_MEDIA_EVENT_CAUSE enumeration [TAPI 2.2], CMC_BAD_DEVICE, CMC_CONNECT_FAIL, CMC_LOCAL_REQUEST, CMC_MEDIA_RECOVERED, CMC_MEDIA_TIMEOUT, CMC_REMOTE_REQUEST, CMC_UNKNOWN, _tapi3_call_media_event_cause, tapi3.call_media_event_cause, tapi3if/CALL_MEDIA_EVENT_CAUSE, tapi3if/CMC_BAD_DEVICE, tapi3if/CMC_CONNECT_FAIL, tapi3if/CMC_LOCAL_REQUEST, tapi3if/CMC_MEDIA_RECOVERED, tapi3if/CMC_MEDIA_TIMEOUT, tapi3if/CMC_REMOTE_REQUEST, tapi3if/CMC_UNKNOWN
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
req.typenames: CALL_MEDIA_EVENT_CAUSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALL_MEDIA_EVENT_CAUSE
 - tapi3if/CALL_MEDIA_EVENT_CAUSE
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
 - CALL_MEDIA_EVENT_CAUSE
---

# CALL_MEDIA_EVENT_CAUSE enumeration


## -description

The 
<b>CALL_MEDIA_EVENT_CAUSE</b> enum is used by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_cause">ITCallMediaEvent::get_Cause</a> method to return a description of what caused a media event, such as a device timeout.

## -enum-fields

### -field CMC_UNKNOWN:0

Call media is unknown.

### -field CMC_BAD_DEVICE

Device source or renderer is not functioning.

### -field CMC_CONNECT_FAIL

Could not connect to media device.

### -field CMC_LOCAL_REQUEST

A local request has been received.

### -field CMC_REMOTE_REQUEST

A remote request has been received.

### -field CMC_MEDIA_TIMEOUT

The media device timed out.

### -field CMC_MEDIA_RECOVERED

Media processing has resumed after an interruption.

### -field CMC_QUALITY_OF_SERVICE

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_cause">ITCallMediaEvent::get_Cause</a>
