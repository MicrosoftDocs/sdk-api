---
UID: NF:rtmv2.RtmReleaseNextHops
title: RtmReleaseNextHops function (rtmv2.h)
author: windows-sdk-content
description: The RtmReleaseNextHops function releases the next-hop handles.
old-location: rras\rtmreleasenexthops.htm
tech.root: RRAS
ms.assetid: a21de428-7e9d-4596-a7ab-06a29b9852f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmReleaseNextHops, RtmReleaseNextHops function [RAS], _rtmv2ref_rtmreleasenexthops, rras.rtmreleasenexthops, rtmv2/RtmReleaseNextHops
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
 - RtmReleaseNextHops
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtmReleaseNextHops function


## -description


The 
<b>RtmReleaseNextHops</b> function releases the next-hop handles.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NumNextHops [in]

Specifies the number of next hops in <i>NextHopHandles</i>.


### -param NextHopHandles [in]

Pointer to an array of next-hop handles to release. The handles were obtained with a previous call to 
<a href="https://msdn.microsoft.com/3e1a6064-6ba0-4ed8-b6df-1c347b098807">RtmGetEnumNextHops</a>.


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




<a href="https://msdn.microsoft.com/d26ce475-ea05-4e84-92da-06df9c386858">RtmCreateNextHopEnum</a>



<a href="https://msdn.microsoft.com/3e1a6064-6ba0-4ed8-b6df-1c347b098807">RtmGetEnumNextHops</a>
 

 

