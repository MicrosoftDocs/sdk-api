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

# _RSVP_STATUS_INFO structure


## -description


The QOS object 
<b>RSVP_STATUS_INFO</b> provides information regarding the status of RSVP for a given flow, including event notifications associated with monitoring FD_QOS events, as well as error information. 
<b>RSVP_STATUS_INFO</b> is useful for storing RSVP-specific status and error information.


## -struct-fields




### -field ObjectHdr

The QOS object 
<b>QOS_OBJECT_HDR</b>.


### -field StatusCode

Status information. See Winsock2.h for more information.


### -field ExtendedStatus1

Mechanism for storing or returning provider-specific status information. The <i>ExtendedStatus1</i> parameter is used for storing a higher-level, or generalized error code, and is augmented by finer-grained error information provided in ExtendedStatus2.


### -field ExtendedStatus2

Additional mechanism for storing or returning provider-specific status information. Provides finer-grained error information compared to the generalized error information provided in <i>ExtendedStatus1</i>.


## -remarks



When applications register their interest in FD_QOS events (see 
<a href="https://msdn.microsoft.com/68c6eff4-d4c0-4b78-858f-e8f8fd4d40b9">QOS Events</a>), event and error information is associated with the event in the form of the 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure that is associated with the event. For more detailed information associated with that event, applications can investigate the <b>RSVP_STATUS_INFO</b> object that is provided in 
<a href="https://msdn.microsoft.com/16c99de7-be29-4e58-b648-b6719385dc1c">the ProviderSpecific buffer</a> of the event-associated 
<b>QOS</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/16c99de7-be29-4e58-b648-b6719385dc1c">ProviderSpecific Buffer</a>



<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>
 

 

