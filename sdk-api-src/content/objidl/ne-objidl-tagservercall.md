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

# tagSERVERCALL enumeration


## -description


Indicates the status of server call.


## -enum-fields




### -field SERVERCALL_ISHANDLED

The object may be able to process the call.


### -field SERVERCALL_REJECTED

The object cannot handle the call due to an unforeseen problem, such as network unavailability.


### -field SERVERCALL_RETRYLATER

The object cannot handle the call at this time. For example, an application might return this value when it is in a user-controlled modal state.


## -see-also




<a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">IMessageFilter::HandleInComingCall</a>



<a href="https://msdn.microsoft.com/3f800819-2a21-4e46-ad15-f9594fac1a3d">IMessageFilter::RetryRejectedCall</a>
 

 

