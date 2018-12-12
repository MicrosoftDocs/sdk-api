---
UID: NS:lpmapi.rsvpmsgobjs
title: RSVP_MSG_OBJS
author: windows-sdk-content
description: The RSVP_MSG_OBJS structure contains RSVP message objects.
old-location: qos\rsvp_msg_objs.htm
tech.root: QOS
ms.assetid: 4ca0bfbc-7c1b-4395-b0fb-487e5c36b5d8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RSVP_MSG_OBJS, RSVP_MSG_OBJS structure [QOS], lpmapi/RSVP_MSG_OBJS, qos.rsvp_msg_objs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Lpmapi.h
api_name:
 - RSVP_MSG_OBJS
product: Windows
targetos: Windows
req.typenames: RSVP_MSG_OBJS
req.redist: 
---

# RSVP_MSG_OBJS structure


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
 

 

