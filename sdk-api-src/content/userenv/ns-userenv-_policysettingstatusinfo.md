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

# _POLICYSETTINGSTATUSINFO structure


## -description


The
    <b>POLICYSETTINGSTATUSINFO</b> structure provides information about a policy-setting event.


## -struct-fields




### -field szKey

This member is optional. If it is <b>NULL</b>, the system generates a value.


### -field szEventSource

Pointer to a string specifying the name of the source (application, service, driver, subsystem) that generated the log entry.


### -field szEventLogName

Pointer to a string specifying the name of the event log.


### -field dwEventID

Specifies the event log message ID.


### -field dwErrorCode

A 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> that indicates an error that occurred during the application of the policy setting.


### -field status

Specifies the status of the policy setting. This member can be one of the following values.



#### RSOPUnspecified

The client-side extension does not define a status for this policy setting.



#### RSOPApplied

The policy setting was applied successfully.



#### RSOPIgnored

The policy setting was ignored; the system made no attempt to apply it.



#### RSOPFailed

Application of the policy setting failed. Details about the failure are indicated by the other members of the structure.



#### RSOPSubsettingFailed

The policy setting was applied successfully, but an error occurred while attempting to apply the child setting.


### -field timeLogged

Specifies a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that indicates the time at which the source generated the event.


## -see-also




<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/7ea2f217-4dd2-4c0f-af1b-d4bcb8707519">RSoPSetPolicySettingStatus</a>
 

 

