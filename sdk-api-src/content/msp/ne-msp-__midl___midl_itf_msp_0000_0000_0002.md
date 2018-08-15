---
UID: NE:msp.__MIDL___MIDL_itf_msp_0000_0000_0002
title: "__MIDL___MIDL_itf_msp_0000_0000_0002"
author: windows-sdk-content
description: The MSP_CALL_EVENT constant is returned within the MSP_EVENT_INFO struct by the GetEvent method when MSP_EVENT is ME_CALL_EVENT.
old-location: tapi3\msp_call_event.htm
old-project: tapi
ms.assetid: c1bbc75e-04ad-4db4-9730-abbbf89306dd
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CALL_NEW_STREAM, CALL_STREAM_ACTIVE, CALL_STREAM_FAIL, CALL_STREAM_INACTIVE, CALL_STREAM_NOT_USED, CALL_TERMINAL_FAIL, MSP_CALL_EVENT, MSP_CALL_EVENT enumeration [TAPI 2.2], __MIDL___MIDL_itf_msp_0000_0000_0002, _tapi3_msp_call_event, msp/CALL_NEW_STREAM, msp/CALL_STREAM_ACTIVE, msp/CALL_STREAM_FAIL, msp/CALL_STREAM_INACTIVE, msp/CALL_STREAM_NOT_USED, msp/CALL_TERMINAL_FAIL, msp/MSP_CALL_EVENT, tapi3.msp_call_event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msp.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSP_CALL_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msp.h
api_name:
 - MSP_CALL_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msp_0000_0000_0002 enumeration


## -description


The <b>MSP_CALL_EVENT</b> constant is returned within the 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> struct by the 
<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">GetEvent</a> method when 
<a href="https://msdn.microsoft.com/53e19eff-b5f0-43fd-b59b-e85e75220282">MSP_EVENT</a> is ME_CALL_EVENT.


## -enum-fields




### -field CALL_NEW_STREAM

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




<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">ITMSPAddress::GetEvent</a>



<a href="https://msdn.microsoft.com/53e19eff-b5f0-43fd-b59b-e85e75220282">MSP_EVENT</a>



<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

