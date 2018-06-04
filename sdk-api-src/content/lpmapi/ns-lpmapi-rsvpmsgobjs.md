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

# rsvpmsgobjs structure


## -description


The 
<b>RSVP_MSG_OBJS</b> structure contains RSVP message objects.


## -struct-fields




### -field RsvpMsgType

RSVP message type.


### -field pRsvpSession

Pointer to an <a href="https://msdn.microsoft.com/d6674de9-7d79-40f2-ae45-4410408ba047">RSVP_SESSION</a> object containing an RSVP session object.


### -field pRsvpFromHop

Pointer to an <a href="https://msdn.microsoft.com/4b23bc0e-ccea-4161-93fa-b136099e88bd">RSVP_HOP</a> structure indicating the hop from which the message has come.


### -field pRsvpToHop

Pointer to an <a href="https://msdn.microsoft.com/4b23bc0e-ccea-4161-93fa-b136099e88bd">RSVP_HOP</a> structure indicating the hop to which the message shall be sent.


### -field pResvStyle

Reservation style, expressed as a <a href="https://msdn.microsoft.com/facc4217-1e6f-44af-bc04-84993f2dfeec">RESV_STYLE</a> structure.


### -field pRsvpScope

Scope of the reservation message.


### -field FlowDescCount

Number of flow descriptors in the message.


### -field pFlowDescs

Pointer to the first <a href="https://msdn.microsoft.com/11ecd7ac-13c4-4f55-9700-105153b4fead">FLOW_DESC</a> structure in the message.


### -field PdObjectCount

Number of policy data objects in the message.


### -field ppPdObjects

Pointer to the first <a href="https://msdn.microsoft.com/0e91b77c-e4dd-4e23-8af6-bf549168cfc5">POLICY_DATA</a> structure in the message.


### -field pErrorSpec

Pointer to an <a href="https://msdn.microsoft.com/4d20cbb8-c29a-4c0c-bf06-532144da3e33">ERROR_SPEC</a> structure containing an error message.


### -field pAdspec

Pointer to an <a href="https://msdn.microsoft.com/c5be3864-0f21-4fa5-99f8-dee9ad2b7286">ADSPEC</a> structure containing an Adspec message.


## -see-also




<a href="https://msdn.microsoft.com/c5be3864-0f21-4fa5-99f8-dee9ad2b7286">ADSPEC</a>



<a href="https://msdn.microsoft.com/4d20cbb8-c29a-4c0c-bf06-532144da3e33">ERROR_SPEC</a>



<a href="https://msdn.microsoft.com/11ecd7ac-13c4-4f55-9700-105153b4fead">FLOW_DESC</a>



<a href="https://msdn.microsoft.com/0e91b77c-e4dd-4e23-8af6-bf549168cfc5">POLICY_DATA</a>



<a href="https://msdn.microsoft.com/facc4217-1e6f-44af-bc04-84993f2dfeec">RESV_STYLE</a>



<a href="https://msdn.microsoft.com/4b23bc0e-ccea-4161-93fa-b136099e88bd">RSVP_HOP</a>



<a href="https://msdn.microsoft.com/d6674de9-7d79-40f2-ae45-4410408ba047">RSVP_SESSION</a>
 

 

