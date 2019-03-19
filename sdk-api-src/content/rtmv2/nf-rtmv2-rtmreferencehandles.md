---
UID: NF:rtmv2.RtmReferenceHandles
title: RtmReferenceHandles function (rtmv2.h)
author: windows-sdk-content
description: The RtmReferenceHandles function increases the reference count for objects pointed to by one or more handles that the routing manager used to access those objects.
old-location: rras\rtmreferencehandles.htm
tech.root: RRAS
ms.assetid: 99031574-a941-451f-ad2e-b99044c9c716
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmReferenceHandles, RtmReferenceHandles function [RAS], _rtmv2ref_rtmreferencehandles, rras.rtmreferencehandles, rtmv2/RtmReferenceHandles
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
 - RtmReferenceHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmReferenceHandles function


## -description


The 
<b>RtmReferenceHandles</b> function increases the reference count for objects pointed to by one or more handles that the routing manager used to access those objects. A client should use this function when the client must keep a handle but release the rest of the information structure associated with the handle.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NumHandles [in]

Specifies the number of handles in <i>RtmHandles</i>.


### -param RtmHandles [in]

Array of handles to increase the reference count for.


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



A client must always call this function when caching a handle returned by the routing table manager. This notifies the routing table manager that it should not destroy the object the handle refers to until the handle is released by the client.

When a client must release the handle, the client must call the appropriate release function, based on the type of handle. For example, to release a route, call 
<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>.




## -see-also




<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>



<a href="https://msdn.microsoft.com/43992abd-7e52-4d1b-b693-f437f5ba77cb">RtmReleaseDestInfo</a>



<a href="https://msdn.microsoft.com/ea72dde4-2d04-4ceb-b718-3ee96bf70464">RtmReleaseEntityInfo</a>



<a href="https://msdn.microsoft.com/1c5a9b72-8605-4c54-bc44-b7a1a4e1b367">RtmReleaseNextHopInfo</a>



<a href="https://msdn.microsoft.com/927d2a32-17bc-453c-b65b-144151bea902">RtmReleaseRouteInfo</a>
 

 

