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

# _NET_VALIDATE_PASSWORD_HASH structure


## -description


The <b>NET_VALIDATE_PASSWORD_HASH</b> structure contains a password hash.


## -struct-fields




### -field Length

Specifies the length of this structure.


### -field Hash

Password hash.


## -remarks



The <a href="https://msdn.microsoft.com/3a6d4c2d-0d90-48bf-9dfa-2ba587538350">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a> and <a href="https://msdn.microsoft.com/09404998-81c5-400c-9d99-a0a4bb4095bf">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a> structures contain a <b>NET_VALIDATE_PASSWORD_HASH</b> structure. The <a href="https://msdn.microsoft.com/1e6ea28a-a007-4cd1-b5d6-686bcf019fa1">NET_VALIDATE_PERSISTED_FIELDS</a> structure contains a pointer to this structure. 




## -see-also




<a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

