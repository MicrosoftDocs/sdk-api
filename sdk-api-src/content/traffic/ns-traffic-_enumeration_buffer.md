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

# _ENUMERATION_BUFFER structure


## -description


The 
<b>ENUMERATION_BUFFER</b> structure contains information specific to a given flow, including flow name, the number of filters associated with the flow, and an array of filters associated with the flow.


## -struct-fields




### -field Length

Number of bytes from the beginning of the 
<b>ENUMERATION_BUFFER</b> to the next 
<b>ENUMERATION_BUFFER</b>.


### -field OwnerProcessId

Identifies the owner of the process.


### -field FlowNameLength

Specifies the length of the <b>FlowName</b> member.


### -field FlowName

Array of WCHAR characters, of length <b>MAX_STRING_LENGTH</b>, that specifies the flow name.


### -field pFlow

Pointer to the corresponding 
<a href="https://msdn.microsoft.com/88b162d9-003c-42ce-8f82-91ee1aa9e32e">TC_GEN_FLOW</a> structure. This structure is placed immediately after the array of TC_GEN_FILTERS and is included in <b>Length</b>.


### -field NumberOfFilters

Specifies the number of filters associated with the flow.


### -field GenericFilter

Array of 
<a href="https://msdn.microsoft.com/979bfa2d-50da-43a6-8ead-d338159e31cf">TC_GEN_FILTER</a> structures. The number of elements in the array corresponds to the number of filters attached to the specified flow. Note that in order to enumerate through the array of 
<b>TC_GEN_FILTER</b> structures, you need to increment the pointer to the current 
<b>TC_GEN_FILTER</b> by using the following: 




sizeof(TC_GEN_FILTER) + 2 * [the pattern size of the current 
<a href="https://msdn.microsoft.com/979bfa2d-50da-43a6-8ead-d338159e31cf">TC_GEN_FILTER</a> structure].


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/979bfa2d-50da-43a6-8ead-d338159e31cf">TC_GEN_FILTER</a>



<a href="https://msdn.microsoft.com/88b162d9-003c-42ce-8f82-91ee1aa9e32e">TC_GEN_FLOW</a>
 

 

