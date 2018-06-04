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

# IKE_AUTHENTICATION_INFORMATION structure


## -description


The <b>IKE_AUTHENTICATION_INFORMATION</b> structure contains Internet Key Exchange (IKE) authentication information used to establish a secure channel between two key management daemons.


## -struct-fields




### -field AuthMethod

A <a href="https://msdn.microsoft.com/be92f3db-93c5-41e3-bd5a-f929f911da39">IKE_AUTHENTICATION_METHOD</a> structure that indicates the authentication method. 


### -field PsKey

A <a href="https://msdn.microsoft.com/52a188b5-6b59-4ea8-89e0-d05440344dde">IKE_AUTHENTICATION_PRESHARED_KEY</a> structure that contains the preshared key that establishes a secure channel between two key management daemons.


## -see-also




<a href="https://msdn.microsoft.com/be92f3db-93c5-41e3-bd5a-f929f911da39">IKE_AUTHENTICATION_METHOD</a>



<a href="https://msdn.microsoft.com/52a188b5-6b59-4ea8-89e0-d05440344dde">IKE_AUTHENTICATION_PRESHARED_KEY</a>
 

 

