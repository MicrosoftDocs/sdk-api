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

# _SECURITY_CAPABILITIES structure


## -description


The <b>SECURITY_CAPABILITIES</b> structure defines the security capabilities of the app container.


## -struct-fields




### -field Capabilities.size_is

 


### -field Capabilities.size_is.CapabilityCount

 


### -field AppContainerSid

The SID of the app container.


### -field Capabilities

The specific capabilities.


### -field CapabilityCount

The number of the capabilities.


### -field Reserved

This member is reserved. Do not use it.


## -see-also




<a href="https://msdn.microsoft.com/CD27774F-0B70-4D97-96C9-B247536CC88E">Capability SID Constants</a>
 

 

