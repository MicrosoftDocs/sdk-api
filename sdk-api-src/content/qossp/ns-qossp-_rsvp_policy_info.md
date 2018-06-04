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

# _RSVP_POLICY_INFO structure


## -description


The <b>RSVP_POLICY_INFO</b> structure stores undefined policy elements retrieved from RSVP.


## -struct-fields




### -field ObjectHdr

QOS object header that specifies the size and length of the QOS object.


### -field NumPolicyElement

Number of policy elements in <b>PolicyElement</b>.


### -field PolicyElement

List of policy elements received, in the form of a <a href="https://msdn.microsoft.com/e23cd113-6fa1-479b-85c2-7690055e57e7">RSVP_POLICY</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>



<a href="https://msdn.microsoft.com/e23cd113-6fa1-479b-85c2-7690055e57e7">RSVP_POLICY</a>
 

 

