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

# _DHCP_POL_COND_ARRAY structure


## -description


The <b>DHCP_POL_COND_ARRAY</b> structure defines an array of DHCP server policy conditions.


## -struct-fields




### -field NumElements

Integer that specifies the number of DHCP server policy conditions in <i>Elements</i>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/99A36029-1CBD-4A93-B25A-A0239D1C08D7">DHCP_POL_COND</a>  structures.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 



