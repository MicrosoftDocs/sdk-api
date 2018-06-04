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

# CALL_STATE_EVENT_CAUSE enumeration


## -description


The 
<b>CALL_STATE_EVENT_CAUSE</b> enum is returned by the 
<a href="https://msdn.microsoft.com/e3a4b985-1c0f-4e93-a965-c61c9c0ab10d">ITCallStateEvent::get_Cause</a> method.


## -enum-fields




### -field CEC_NONE

No call event has occurred.


### -field CEC_DISCONNECT_NORMAL

The call was disconnected as part of the normal life cycle of the call (that is, the call was over, so it was disconnected).


### -field CEC_DISCONNECT_BUSY

An outgoing call failed to connect because the remote end was busy.


### -field CEC_DISCONNECT_BADADDRESS

An outgoing call failed because the destination address was bad.


### -field CEC_DISCONNECT_NOANSWER

An outgoing call failed because the remote end was not answered.


### -field CEC_DISCONNECT_CANCELLED

An outgoing call failed because the caller disconnected.


### -field CEC_DISCONNECT_REJECTED

The outgoing call was rejected by the remote end.


### -field CEC_DISCONNECT_FAILED

The call failed to connect for some other reason.


### -field CEC_DISCONNECT_BLOCKED




## -see-also




<a href="https://msdn.microsoft.com/e3a4b985-1c0f-4e93-a965-c61c9c0ab10d">ITCallStateEvent::get_Cause</a>
 

 

