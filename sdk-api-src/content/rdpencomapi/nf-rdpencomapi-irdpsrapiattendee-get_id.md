---
UID: NF:rdpencomapi.IRDPSRAPIAttendee.get_Id
title: IRDPSRAPIAttendee::get_Id
author: windows-sdk-content
description: The unique identifier for the attendee.
old-location: rdp\irdpsrapiattendee_id.htm
old-project: rdp
ms.assetid: 9ed04c11-d3cc-4846-88e8-aad9fb23fee8
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CONST_ATTENDEE_ID_DEFAULT, IRDPSRAPIAttendee interface [RDP],Id property, IRDPSRAPIAttendee.Id, IRDPSRAPIAttendee.get_Id, IRDPSRAPIAttendee::Id, IRDPSRAPIAttendee::get_Id, Id property [RDP], Id property [RDP],IRDPSRAPIAttendee interface, Id property [RDP],RDPSRAPIAttendee object, RDPSRAPIAttendee object [RDP],Id property, get_Id, rdp.irdpsrapiattendee_id, rdpencomapi/IRDPSRAPIAttendee::Id, rdpencomapi/IRDPSRAPIAttendee::get_Id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAttendee.Id
 - IRDPSRAPIAttendee.get_Id
 - RDPSRAPIAttendee.Id
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPIAttendee::get_Id


## -description


The unique identifier for the attendee.

This property is read-only.


## -parameters


## -remarks



If an attendee disconnects, the attendee object will be destroyed. If the attendee reconnects, a new object will be created with a new identifier.




## -see-also




<a href="https://msdn.microsoft.com/e9edd9f2-ccbf-45b2-b71c-e30368435a60">IRDPSRAPIAttendee</a>



<a href="https://msdn.microsoft.com/50c56089-75f9-41c9-a4a4-10556f98d6e8">RDPENCOMAPI_CONSTANTS</a>
 

 

