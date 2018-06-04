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

# _UPDATE_COMPLETE_MESSAGE structure


## -description


The 
<b>UPDATE_COMPLETE_MESSAGE</b> structure contains information describing the completion status of an update operation.


## -struct-fields




### -field InterfaceIndex

Identifies the interface over which the update was performed.


### -field UpdateType

Indicates the type of information that was received in this update. This member is one of the following values: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEMAND_UPDATE_ROUTES"></a><a id="demand_update_routes"></a><dl>
<dt><b>DEMAND_UPDATE_ROUTES</b></dt>
</dl>
</td>
<td width="60%">
Routing information was reported to the routing table manager.

</td>
</tr>
<tr>
<td width="40%"><a id="DEMAND_UPDATE_SERVICES"></a><a id="demand_update_services"></a><dl>
<dt><b>DEMAND_UPDATE_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
Services information that is accessible through the Services Table Management functions provided by the routing protocol.

</td>
</tr>
</table>
 


### -field UpdateStatus


Indicates the result of the update operation. 


					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NO_ERROR"></a><a id="no_error"></a><dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The update was completed successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_CAN_NOT_COMPLETE"></a><a id="error_can_not_complete"></a><dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The update was unsuccessful.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/94f3069f-c282-4dea-84f9-48645f4e1593">MESSAGE</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/679c74fa-0049-4556-a942-e51160ceb796">Routing Protocol Interface Structures</a>
 

 

