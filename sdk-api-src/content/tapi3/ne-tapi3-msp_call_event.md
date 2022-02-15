---
UID: NE:tapi3.__MIDL___MIDL_itf_tapi3_0000_0018_0002
title: MSP_CALL_EVENT (tapi3.h)
description: The MSP_CALL_EVENT constant is returned within the MSP_EVENT_INFO struct by the GetEvent method when MSP_EVENT is ME_CALL_EVENT.
helpviewer_keywords: ["CALL_NEW_STREAM","CALL_STREAM_ACTIVE","CALL_STREAM_FAIL","CALL_STREAM_INACTIVE","CALL_STREAM_NOT_USED","CALL_TERMINAL_FAIL","MSP_CALL_EVENT","MSP_CALL_EVENT enumeration [TAPI 2.2]","_tapi3_msp_call_event","msp/CALL_NEW_STREAM","msp/CALL_STREAM_ACTIVE","msp/CALL_STREAM_FAIL","msp/CALL_STREAM_INACTIVE","msp/CALL_STREAM_NOT_USED","msp/CALL_TERMINAL_FAIL","msp/MSP_CALL_EVENT","tapi3.msp_call_event"]
old-location: tapi3\msp_call_event.htm
tech.root: tapi3
ms.assetid: c1bbc75e-04ad-4db4-9730-abbbf89306dd
ms.date: 12/05/2018
ms.keywords: CALL_NEW_STREAM, CALL_STREAM_ACTIVE, CALL_STREAM_FAIL, CALL_STREAM_INACTIVE, CALL_STREAM_NOT_USED, CALL_TERMINAL_FAIL, MSP_CALL_EVENT, MSP_CALL_EVENT enumeration [TAPI 2.2], _tapi3_msp_call_event, msp/CALL_NEW_STREAM, msp/CALL_STREAM_ACTIVE, msp/CALL_STREAM_FAIL, msp/CALL_STREAM_INACTIVE, msp/CALL_STREAM_NOT_USED, msp/CALL_TERMINAL_FAIL, msp/MSP_CALL_EVENT, tapi3.msp_call_event
req.header: tapi3.h
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
req.typenames: MSP_CALL_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_tapi3_0000_0018_0002
 - tapi3/__MIDL___MIDL_itf_tapi3_0000_0018_0002
 - MSP_CALL_EVENT
 - tapi3/MSP_CALL_EVENT
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
 - MSP_CALL_EVENT
---

# MSP_CALL_EVENT enumeration


## -description

The <b>MSP_CALL_EVENT</b> constant is returned within the 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> struct by the 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">GetEvent</a> method when 
<a href="/windows/win32/api/msp/ne-msp-msp_event">MSP_EVENT</a> is ME_CALL_EVENT.

## -enum-fields

### -field CALL_NEW_STREAM:0

A new stream is created by the call. The application can choose to select a terminal or delete the stream from the call.

### -field CALL_STREAM_FAIL

Setup of the stream failed or the stream fails to start.

### -field CALL_TERMINAL_FAIL

The terminal failed to connect.

### -field CALL_STREAM_NOT_USED

The stream is not used in the call (the remote party rejected it).

### -field CALL_STREAM_ACTIVE

The application needs this event to decide when a stream can be used to send and receive data. It is fired when the streams enter running state (the timing of which is determined by the TSP).

### -field CALL_STREAM_INACTIVE

No more data can be sent to or received from this stream. This happens when a send stream has sent all its data, or when a receive stream stops receiving data.

## -see-also

<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">ITMSPAddress::GetEvent</a>



<a href="/windows/win32/api/msp/ne-msp-msp_event">MSP_EVENT</a>



<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
