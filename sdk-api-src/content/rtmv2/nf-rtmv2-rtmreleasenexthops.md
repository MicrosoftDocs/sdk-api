---
UID: NF:rtmv2.RtmReleaseNextHops
title: RtmReleaseNextHops function (rtmv2.h)

description: The RtmReleaseNextHops function releases the next-hop handles.
old-location: rras\rtmreleasenexthops.htm
tech.root: RRAS
ms.assetid: a21de428-7e9d-4596-a7ab-06a29b9852f7

ms.date: 12/05/2018
ms.keywords: RtmReleaseNextHops, RtmReleaseNextHops function [RAS], _rtmv2ref_rtmreleasenexthops, rras.rtmreleasenexthops, rtmv2/RtmReleaseNextHops
ms.topic: function
f1_keywords: 
 - "rtmv2/RtmReleaseNextHops"
dev_langs:
 - c++
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.


### -param NumNextHops [in]

Specifies the number of next hops in <i>NextHopHandles</i>.


### -param NextHopHandles [in]

Pointer to an array of next-hop handles to release. The handles were obtained with a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumnexthops">RtmGetEnumNextHops</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatenexthopenum">RtmCreateNextHopEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumnexthops">RtmGetEnumNextHops</a>
 

 

