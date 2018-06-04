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

# _RTM_NEXTHOP_INFO structure


## -description


The 
<b>RTM_NEXTHOP_INFO</b> structure is used to exchange next-hop information with the routing table manager.
			


## -struct-fields




### -field NextHopAddress

Specifies the network address for this next hop.


### -field NextHopOwner

Handle to the client that owns this next hop.


### -field InterfaceIndex

Specifies the outgoing interface index.


### -field State

Flags that indicates the state of this next hop. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_NEXTHOP_STATE_CREATED"></a><a id="rtm_nexthop_state_created"></a><dl>
<dt><b>RTM_NEXTHOP_STATE_CREATED</b></dt>
</dl>
</td>
<td width="60%">
The next hop has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_NEXTHOP_STATE_DELETED"></a><a id="rtm_nexthop_state_deleted"></a><dl>
<dt><b>RTM_NEXTHOP_STATE_DELETED</b></dt>
</dl>
</td>
<td width="60%">
The next hop has been deleted.

</td>
</tr>
</table>
 


### -field Flags

Flags that convey status information for the next hop. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_NEXTHOP_FLAGS_REMOTE"></a><a id="rtm_nexthop_flags_remote"></a><dl>
<dt><b>RTM_NEXTHOP_FLAGS_REMOTE</b></dt>
</dl>
</td>
<td width="60%">
This next hop points to a remote destination that is not directly reachable. To obtain the complete path, the client must perform a recursive lookup.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_NEXTHOP_FLAGS_DOWN"></a><a id="rtm_nexthop_flags_down"></a><dl>
<dt><b>RTM_NEXTHOP_FLAGS_DOWN</b></dt>
</dl>
</td>
<td width="60%">
This flag is reserved for future use.

</td>
</tr>
</table>
 


### -field EntitySpecificInfo

Contains information specific to the client that owns this next hop.


### -field RemoteNextHop

Handle to the destination with the indirect next-hop address. This member is only valid when the <b>Flags</b> member is set to RTM_NEXTHOP_FLAGS_REMOTE. This cached handle can prevent multiple lookups for this indirect next hop.


## -see-also




<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a>



<a href="https://msdn.microsoft.com/7c11397b-f5c9-4a3e-88d8-2f1736f5da13">RtmAddNextHop</a>



<a href="https://msdn.microsoft.com/708a890e-4dc6-49c7-b857-cdb8504e7f7f">RtmDeleteNextHop</a>



<a href="https://msdn.microsoft.com/82bf88ad-eb6d-4ea5-98a0-72280e341f83">RtmFindNextHop</a>



<a href="https://msdn.microsoft.com/45f18cfe-b863-4b78-90e4-c7b25c949834">RtmGetNextHopInfo</a>



<a href="https://msdn.microsoft.com/61fa3fa2-1cad-4930-975e-8f5b86ad3b05">RtmGetNextHopPointer</a>



<a href="https://msdn.microsoft.com/f5b6d430-a50e-49fc-8274-81bac1300477">RtmLockNextHop</a>



<a href="https://msdn.microsoft.com/1c5a9b72-8605-4c54-bc44-b7a1a4e1b367">RtmReleaseNextHopInfo</a>
 

 

