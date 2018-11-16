---
UID: NE:tapi3.__MIDL___MIDL_itf_tapi3_0000_0018_0003
title: "__MIDL___MIDL_itf_tapi3_0000_0018_0003"
author: windows-sdk-content
description: The MSP_CALL_EVENT_CAUSE constant is returned within the MSP_EVENT_INFO struct by the GetEvent method when MSP_EVENT is ME_CALL_EVENT.
old-location: tapi3\msp_call_event_cause.htm
tech.root: Tapi
ms.assetid: 3724bead-d16a-40dd-b55c-3c31846f1c1c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CALL_CAUSE_BAD_DEVICE, CALL_CAUSE_CONNECT_FAIL, CALL_CAUSE_LOCAL_REQUEST, CALL_CAUSE_MEDIA_RECOVERED, CALL_CAUSE_MEDIA_TIMEOUT, CALL_CAUSE_REMOTE_REQUEST, CALL_CAUSE_UNKNOWN, MSP_CALL_EVENT_CAUSE, MSP_CALL_EVENT_CAUSE enumeration [TAPI 2.2], __MIDL___MIDL_itf_tapi3_0000_0018_0003, _tapi3_msp_call_event_cause, msp/CALL_CAUSE_BAD_DEVICE, msp/CALL_CAUSE_CONNECT_FAIL, msp/CALL_CAUSE_LOCAL_REQUEST, msp/CALL_CAUSE_MEDIA_RECOVERED, msp/CALL_CAUSE_MEDIA_TIMEOUT, msp/CALL_CAUSE_REMOTE_REQUEST, msp/CALL_CAUSE_UNKNOWN, msp/MSP_CALL_EVENT_CAUSE, tapi3.msp_call_event_cause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msp.h
api_name:
 - MSP_CALL_EVENT_CAUSE
product: Windows
targetos: Windows
req.typenames: MSP_CALL_EVENT_CAUSE
req.redist: 
---

# __MIDL___MIDL_itf_tapi3_0000_0018_0003 enumeration


## -description


The <b>MSP_CALL_EVENT_CAUSE</b> constant is returned within the 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> struct by the 
<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">GetEvent</a> method when 
<a href="https://msdn.microsoft.com/53e19eff-b5f0-43fd-b59b-e85e75220282">MSP_EVENT</a> is ME_CALL_EVENT.


## -enum-fields




### -field CALL_CAUSE_UNKNOWN

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




<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">ITMSPAddress::GetEvent</a>



<a href="https://msdn.microsoft.com/53e19eff-b5f0-43fd-b59b-e85e75220282">MSP_EVENT</a>



<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

