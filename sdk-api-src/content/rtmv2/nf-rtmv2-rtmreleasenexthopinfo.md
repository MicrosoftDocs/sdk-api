---
UID: NF:rtmv2.RtmReleaseNextHopInfo
title: RtmReleaseNextHopInfo function
author: windows-sdk-content
description: The RtmReleaseNextHopInfo function releases a next-hop structure.
old-location: rras\rtmreleasenexthopinfo.htm
old-project: rras
ms.assetid: 1c5a9b72-8605-4c54-bc44-b7a1a4e1b367
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: RtmReleaseNextHopInfo, RtmReleaseNextHopInfo function [RAS], _rtmv2ref_rtmreleasenexthopinfo, rras.rtmreleasenexthopinfo, rtmv2/RtmReleaseNextHopInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmReleaseNextHopInfo
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: ADAM
---

# RtmReleaseNextHopInfo function


## -description


The 
<b>RtmReleaseNextHopInfo</b> function releases a next-hop structure.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NextHopInfo [in]

Pointer to the 
<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a> structure to release. The next hop was obtained with a previous call to 
<a href="https://msdn.microsoft.com/45f18cfe-b863-4b78-90e4-c7b25c949834">RtmGetNextHopInfo</a>.


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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a>



<a href="https://msdn.microsoft.com/82bf88ad-eb6d-4ea5-98a0-72280e341f83">RtmFindNextHop</a>



<a href="https://msdn.microsoft.com/45f18cfe-b863-4b78-90e4-c7b25c949834">RtmGetNextHopInfo</a>
 

 

