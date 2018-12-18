---
UID: NS:rtmv2._RTM_NEXTHOP_INFO
title: RTM_NEXTHOP_INFO
author: windows-sdk-content
description: The RTM_NEXTHOP_INFO structure is used to exchange next-hop information with the routing table manager.
old-location: rras\rtm_nexthop_info.htm
tech.root: rras
ms.assetid: 17705e5b-0905-45a5-b76e-e381e863a1ea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRTM_NEXTHOP_INFO, PRTM_NEXTHOP_INFO, PRTM_NEXTHOP_INFO structure pointer [RAS], RTM_NEXTHOP_FLAGS_DOWN, RTM_NEXTHOP_FLAGS_REMOTE, RTM_NEXTHOP_INFO, RTM_NEXTHOP_INFO structure [RAS], RTM_NEXTHOP_STATE_CREATED, RTM_NEXTHOP_STATE_DELETED, _rtmv2ref_rtm_nexthop_info, rras.rtm_nexthop_info, rtmv2/PRTM_NEXTHOP_INFO, rtmv2/RTM_NEXTHOP_INFO"
ms.topic: struct
req.header: rtmv2.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_NEXTHOP_INFO
product: Windows
targetos: Windows
req.typenames: RTM_NEXTHOP_INFO, *PRTM_NEXTHOP_INFO
req.redist: 
---

# RTM_NEXTHOP_INFO structure


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
 

 

