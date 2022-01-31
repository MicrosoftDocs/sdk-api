---
UID: NE:msp.__MIDL___MIDL_itf_msp_0000_0000_0003
title: MSP_CALL_EVENT_CAUSE (msp.h)
description: The MSP_CALL_EVENT_CAUSE constant is returned within the MSP_EVENT_INFO struct by the GetEvent method when MSP_EVENT is ME_CALL_EVENT.
helpviewer_keywords: ["CALL_CAUSE_BAD_DEVICE","CALL_CAUSE_CONNECT_FAIL","CALL_CAUSE_LOCAL_REQUEST","CALL_CAUSE_MEDIA_RECOVERED","CALL_CAUSE_MEDIA_TIMEOUT","CALL_CAUSE_REMOTE_REQUEST","CALL_CAUSE_UNKNOWN","MSP_CALL_EVENT_CAUSE","MSP_CALL_EVENT_CAUSE enumeration [TAPI 2.2]","_tapi3_msp_call_event_cause","msp/CALL_CAUSE_BAD_DEVICE","msp/CALL_CAUSE_CONNECT_FAIL","msp/CALL_CAUSE_LOCAL_REQUEST","msp/CALL_CAUSE_MEDIA_RECOVERED","msp/CALL_CAUSE_MEDIA_TIMEOUT","msp/CALL_CAUSE_REMOTE_REQUEST","msp/CALL_CAUSE_UNKNOWN","msp/MSP_CALL_EVENT_CAUSE","tapi3.msp_call_event_cause"]
old-location: tapi3\msp_call_event_cause.htm
tech.root: tapi3
ms.assetid: 3724bead-d16a-40dd-b55c-3c31846f1c1c
ms.date: 12/05/2018
ms.keywords: CALL_CAUSE_BAD_DEVICE, CALL_CAUSE_CONNECT_FAIL, CALL_CAUSE_LOCAL_REQUEST, CALL_CAUSE_MEDIA_RECOVERED, CALL_CAUSE_MEDIA_TIMEOUT, CALL_CAUSE_REMOTE_REQUEST, CALL_CAUSE_UNKNOWN, MSP_CALL_EVENT_CAUSE, MSP_CALL_EVENT_CAUSE enumeration [TAPI 2.2], _tapi3_msp_call_event_cause, msp/CALL_CAUSE_BAD_DEVICE, msp/CALL_CAUSE_CONNECT_FAIL, msp/CALL_CAUSE_LOCAL_REQUEST, msp/CALL_CAUSE_MEDIA_RECOVERED, msp/CALL_CAUSE_MEDIA_TIMEOUT, msp/CALL_CAUSE_REMOTE_REQUEST, msp/CALL_CAUSE_UNKNOWN, msp/MSP_CALL_EVENT_CAUSE, tapi3.msp_call_event_cause
req.header: msp.h
req.include-header: Tapi3.h
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
req.typenames: MSP_CALL_EVENT_CAUSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msp_0000_0000_0003
 - msp/__MIDL___MIDL_itf_msp_0000_0000_0003
 - MSP_CALL_EVENT_CAUSE
 - msp/MSP_CALL_EVENT_CAUSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msp.h
api_name:
 - MSP_CALL_EVENT_CAUSE
---

# MSP_CALL_EVENT_CAUSE enumeration


## -description

The <b>MSP_CALL_EVENT_CAUSE</b> constant is returned within the 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> struct by the 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">GetEvent</a> method when 
<a href="/windows/win32/api/msp/ne-msp-msp_event">MSP_EVENT</a> is ME_CALL_EVENT.

## -enum-fields

### -field CALL_CAUSE_UNKNOWN:0

Call event cause is unknown.

### -field CALL_CAUSE_BAD_DEVICE

A bad device caused failure, for either STREAM_FAIL or TERMINAL_FAIL.

### -field CALL_CAUSE_CONNECT_FAIL

Either connecting the stream failed or connecting the terminal failed. Note that if a terminal cannot be connected to a stream, the application will get a TERMINAL_FAIL event with CMC_CONNECT_FAIL. If this stream failed because the terminal is the only one to use, the application will also get a STREAM_FAIL event with CMC_CONNECT_FAIL.

### -field CALL_CAUSE_LOCAL_REQUEST

The event is the result of the application calling a method on the stream.

### -field CALL_CAUSE_REMOTE_REQUEST

The event is the result of the remote endpoint's request.

### -field CALL_CAUSE_MEDIA_TIMEOUT

The media that carries the stream is temporarily not available.

### -field CALL_CAUSE_MEDIA_RECOVERED

The media that carries the stream is back to normal from a temporary denial of service.

### -field CALL_CAUSE_QUALITY_OF_SERVICE

## -see-also

<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">ITMSPAddress::GetEvent</a>



<a href="/windows/win32/api/msp/ne-msp-msp_event">MSP_EVENT</a>



<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
