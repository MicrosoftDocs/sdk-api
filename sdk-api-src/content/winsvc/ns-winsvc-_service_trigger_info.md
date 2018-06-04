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

# _SERVICE_TRIGGER_INFO structure


## -description


Contains trigger event information for a service. This structure is used by the <a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a> and <a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a> functions.


## -struct-fields




### -field cTriggers

The number of triggers in the array of <a href="https://msdn.microsoft.com/a57aa702-40a2-4880-80db-6c4f43c3e7ea">SERVICE_TRIGGER</a> structures pointed to by the <b>pTriggers</b> member.  

If this member is 0 in a <b>SERVICE_TRIGGER_INFO</b> structure passed to  <a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>, all previously configured triggers are removed from the service. If the service has no triggers configured, <b>ChangeServiceConfig2</b>  fails with ERROR_INVALID_PARAMETER.


### -field cTriggers.range

 


### -field cTriggers.range.0

 


### -field cTriggers.range.64

 


### -field pTriggers

A pointer to an array of <a href="https://msdn.microsoft.com/a57aa702-40a2-4880-80db-6c4f43c3e7ea">SERVICE_TRIGGER</a> structures that specify the trigger events for the service. If the <b>cTriggers</b> member is 0, this member is not used.


### -field pTriggers.size_is

 


### -field pTriggers.size_is.cTriggers

 


### -field pReserved

This member is reserved and must be NULL.


## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/a57aa702-40a2-4880-80db-6c4f43c3e7ea">SERVICE_TRIGGER</a>



<a href="https://msdn.microsoft.com/ca02a3ae-b16a-4427-b6db-b935c9cf23b3">Service Trigger Events</a>
 

 

