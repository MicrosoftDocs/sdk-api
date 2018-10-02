---
UID: NF:rtmv2.RtmGetNextHopInfo
title: RtmGetNextHopInfo function
author: windows-sdk-content
description: The RtmGetNextHopInfo function returns information about the specified next hop.
old-location: rras\rtmgetnexthopinfo.htm
tech.root: RRAS
ms.assetid: 45f18cfe-b863-4b78-90e4-c7b25c949834
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RtmGetNextHopInfo, RtmGetNextHopInfo function [RAS], _rtmv2ref_rtmgetnexthopinfo, rras.rtmgetnexthopinfo, rtmv2/RtmGetNextHopInfo
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
 - RtmGetNextHopInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmGetNextHopInfo function


## -description


The 
<b>RtmGetNextHopInfo</b> function returns information about the specified next hop.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NextHopHandle [in]

Handle to the next hop.


### -param NextHopInfo [out]

On input, <i>NextHopInfo</i> a pointer to an 
<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a> structure. 




On output, <i>NextHopInfo</i> is filled with the requested next-hop information.


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





## -remarks



When the next hop handle is no longer required, release it by calling 
<a href="https://msdn.microsoft.com/708a890e-4dc6-49c7-b857-cdb8504e7f7f">RtmDeleteNextHop</a>.




## -see-also




<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a>



<a href="https://msdn.microsoft.com/1c5a9b72-8605-4c54-bc44-b7a1a4e1b367">RtmReleaseNextHopInfo</a>
 

 

