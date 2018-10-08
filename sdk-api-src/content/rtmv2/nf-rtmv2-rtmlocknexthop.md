---
UID: NF:rtmv2.RtmLockNextHop
title: RtmLockNextHop function
author: windows-sdk-content
description: The RtmLockNextHop function locks or unlocks a next hop. This function should be called by the next hop's owner to lock the next hop before making changes to the next hop. A pointer to the next hop is returned.
old-location: rras\rtmlocknexthop.htm
tech.root: rras
ms.assetid: f5b6d430-a50e-49fc-8274-81bac1300477
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: RtmLockNextHop, RtmLockNextHop function [RAS], _rtmv2ref_rtmlocknexthop, rras.rtmlocknexthop, rtmv2/RtmLockNextHop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmLockNextHop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmLockNextHop function


## -description


The 
<b>RtmLockNextHop</b> function locks or unlocks a next hop. This function should be called by the next hop's owner to lock the next hop before making changes to the next hop. A pointer to the next hop is returned.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NextHopHandle [in]

Handle to the next hop to lock or unlock.


### -param Exclusive [in]

Specifies whether to lock or unlock the next hop in an exclusive (<b>TRUE</b>) or shared (<b>FALSE</b>) mode.


### -param LockNextHop [in]

Specifies whether to lock or unlock the next hop. Specify <b>TRUE</b> to lock the next hop; specify <b>FALSE</b> to unlock it.


### -param NextHopPointer [out]

On input, <i>NextHopPointer</i> is a pointer to <b>NULL</b>. 




On output, if the client owns the next hop, <i>NextHopPointer</i> receives a pointer to the next-hop; otherwise, <i>NextHopPointer</i> remains unchanged.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling client does not own this next hop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified next hop was not found.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



Clients cannot change the <b>NextHopAddress</b> and <b>InterfaceIndex</b> members of the <a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a> structure; these values are used to uniquely identify a next hop.




## -see-also




<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a>



<a href="https://msdn.microsoft.com/7c11397b-f5c9-4a3e-88d8-2f1736f5da13">RtmAddNextHop</a>



<a href="https://msdn.microsoft.com/708a890e-4dc6-49c7-b857-cdb8504e7f7f">RtmDeleteNextHop</a>



<a href="https://msdn.microsoft.com/82bf88ad-eb6d-4ea5-98a0-72280e341f83">RtmFindNextHop</a>



<a href="https://msdn.microsoft.com/61fa3fa2-1cad-4930-975e-8f5b86ad3b05">RtmGetNextHopPointer</a>
 

 

