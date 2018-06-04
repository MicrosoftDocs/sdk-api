---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

