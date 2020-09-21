---
UID: NS:routprot._UPDATE_COMPLETE_MESSAGE
title: UPDATE_COMPLETE_MESSAGE (routprot.h)
description: The UPDATE_COMPLETE_MESSAGE structure contains information describing the completion status of an update operation.
helpviewer_keywords: ["*PUPDATE_COMPLETE_MESSAGE","DEMAND_UPDATE_ROUTES","DEMAND_UPDATE_SERVICES","ERROR_CAN_NOT_COMPLETE","NO_ERROR","PUPDATE_COMPLETE_MESSAGE","PUPDATE_COMPLETE_MESSAGE structure pointer [RAS]","UPDATE_COMPLETE_MESSAGE","UPDATE_COMPLETE_MESSAGE structure [RAS]","_mpr_update_complete_message","routprot/PUPDATE_COMPLETE_MESSAGE","routprot/UPDATE_COMPLETE_MESSAGE","rras.update_complete_message"]
old-location: rras\update_complete_message.htm
tech.root: RRAS
ms.assetid: 76f00da0-4f56-4a1a-977d-a3872bbe19fc
ms.date: 12/05/2018
ms.keywords: '*PUPDATE_COMPLETE_MESSAGE, DEMAND_UPDATE_ROUTES, DEMAND_UPDATE_SERVICES, ERROR_CAN_NOT_COMPLETE, NO_ERROR, PUPDATE_COMPLETE_MESSAGE, PUPDATE_COMPLETE_MESSAGE structure pointer [RAS], UPDATE_COMPLETE_MESSAGE, UPDATE_COMPLETE_MESSAGE structure [RAS], _mpr_update_complete_message, routprot/PUPDATE_COMPLETE_MESSAGE, routprot/UPDATE_COMPLETE_MESSAGE, rras.update_complete_message'
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UPDATE_COMPLETE_MESSAGE, *PUPDATE_COMPLETE_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UPDATE_COMPLETE_MESSAGE
 - routprot/_UPDATE_COMPLETE_MESSAGE
 - PUPDATE_COMPLETE_MESSAGE
 - routprot/PUPDATE_COMPLETE_MESSAGE
 - UPDATE_COMPLETE_MESSAGE
 - routprot/UPDATE_COMPLETE_MESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - UPDATE_COMPLETE_MESSAGE
---

# UPDATE_COMPLETE_MESSAGE structure


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

<a href="/windows/desktop/api/routprot/ns-routprot-message">MESSAGE</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-structures">Routing Protocol Interface Structures</a>