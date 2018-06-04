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

# _FLOWDESCRIPTOR structure


## -description


The <b>FLOWDESCRIPTOR</b> structure specifies one or more filters for a given FLOWSPEC.


## -struct-fields




### -field FlowSpec

Flow specification (FLOWSPEC), provided as a <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure.


### -field NumFilters

Number of filters provided in <b>FilterList</b>.


### -field FilterList

Pointer to a <a href="https://msdn.microsoft.com/ce4af25d-6c31-43a2-a30a-1d28b18e8f8b">RSVP_FILTERSPEC</a> structure containing FILTERSPEC information.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/ce4af25d-6c31-43a2-a30a-1d28b18e8f8b">RSVP_FILTERSPEC</a>
 

 

