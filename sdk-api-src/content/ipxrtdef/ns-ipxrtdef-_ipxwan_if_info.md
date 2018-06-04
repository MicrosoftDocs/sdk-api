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

# _IPXWAN_IF_INFO structure


## -description


The 
<b>IPXWAN_IF_INFO</b> structure stores the administrative state for an IPX WAN interface.


## -struct-fields




### -field AdminState

Specifies the administrative state of the interface. This member can be one of the following values. These value are defined in Ipxconst.h. 




ADMIN_STATE_DISABLED

ADMIN_STATE_ENABLED

ADMIN_STATE_ENABLED_ONLY_FOR_NETBIOS_STATIC_ROUTING

ADMIN_STATE_ENABLED_ONLY_FOR_OPER_STATE_UP


## -see-also




<a href="https://msdn.microsoft.com/f1c07033-dbfa-4bbe-b275-f5bfc629b2d7">IPX_IF_INFO</a>



<a href="https://msdn.microsoft.com/389002c9-2d24-4b35-ab5b-801fe2091db9">MprInfo Functions and Information Headers</a>
 

 

