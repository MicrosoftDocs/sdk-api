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

# RSVP_SCOPE structure


## -description


The 
<b>RSVP_SCOPE</b> structure provides RSVP scope information.


## -struct-fields




### -field scopl_header

Scope header, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field scope_u

Union containing scope list information.


### -field scope_u.scopl_ipv4

RSVP scope list, in the form of a <a href="https://msdn.microsoft.com/f1651371-d192-45d9-9a9e-d272b624f40d">Scope_list_ipv4</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>



<a href="https://msdn.microsoft.com/f1651371-d192-45d9-9a9e-d272b624f40d">Scope_list_ipv4</a>
 

 

