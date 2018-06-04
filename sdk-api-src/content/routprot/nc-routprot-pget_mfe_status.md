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

# PGET_MFE_STATUS callback function


## -description


The router manager calls the 
<b>GetMfeStatus</b> function to obtain the status of the multicast forwarding entry (MFE) for the specified interface, group address, and source address.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PGET_MFE_STATUS</a> type defines a pointer to this callback function. <i>GetMfeStatus</i> is a placeholder for the application-defined function name.


## -parameters




### -param InterfaceIndex [in]

Specifies the index of the interface for this MFE.


### -param GroupAddress [in]

Specifies the multicast group address for this MFE.


### -param SourceAddress [in]

Specifies the multicast source address for this MFE.


### -param StatusCode [out]

Pointer to a <b>BYTE</b> variable. The routing protocol should fill in this variable with one of the following values. The routing protocol should select the highest-valued code that applies. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFE_NO_ERROR"></a><a id="mfe_no_error"></a><dl>
<dt><b>MFE_NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
None of the following values apply.

</td>
</tr>
<tr>
<td width="40%"><a id="MFE_REACHED_CORE"></a><a id="mfe_reached_core"></a><dl>
<dt><b>MFE_REACHED_CORE</b></dt>
</dl>
</td>
<td width="60%">
The local computer on this router is an rendezvous point (RP)/core router for the multicast group.

</td>
</tr>
<tr>
<td width="40%"><a id="MFE_OIF_PRUNED"></a><a id="mfe_oif_pruned"></a><dl>
<dt><b>MFE_OIF_PRUNED</b></dt>
</dl>
</td>
<td width="60%">
This value should be set only by the owner of the outgoing interface. The value indicates that no downstream receivers exist on the outgoing interface.

</td>
</tr>
<tr>
<td width="40%"><a id="MFE_PRUNED_UPSTREAM"></a><a id="mfe_pruned_upstream"></a><dl>
<dt><b>MFE_PRUNED_UPSTREAM</b></dt>
</dl>
</td>
<td width="60%">
This value should be set only by the owner of the incoming interface. The value indicates that a prune message was sent upstream.

</td>
</tr>
<tr>
<td width="40%"><a id="MFE_OLD_ROUTER"></a><a id="mfe_old_router"></a><dl>
<dt><b>MFE_OLD_ROUTER</b></dt>
</dl>
</td>
<td width="60%">
This value should be set only by the owner of the incoming interface. The value indicates that the upstream neighbor doesn't support mtrace.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value should be NO_ERROR.

If the function fails, the return value should be one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol could not complete the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, no interface exists with that index), or the group or source address is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



Only multicast routing protocols need implement this function. Non-multicast routing protocols should pass <b>NULL</b> as the pointer value for this function in 
<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a>





## -see-also




<a href="https://msdn.microsoft.com/31a28a43-3cfd-4d3c-813e-8f8289d99712">GetNeighbors</a>
 

 

