---
UID: NF:rtmv2.RtmGetLessSpecificDestination
title: RtmGetLessSpecificDestination function
author: windows-driver-content
description: The RtmGetLessSpecificDestination function searches the routing table for a destination with the next-best-match (longest) prefix, given a destination prefix. The requested destination information is returned.
old-location: rras\rtmgetlessspecificdestination.htm
old-project: RRAS
ms.assetid: b6ff1b1f-fd0e-4cfb-9030-67e27e8578f6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: RtmGetLessSpecificDestination, RtmGetLessSpecificDestination function [RAS], _rtmv2ref_rtmgetlessspecificdestination, rras.rtmgetlessspecificdestination, rtmv2/RtmGetLessSpecificDestination
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
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	RtmGetLessSpecificDestination
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmGetLessSpecificDestination function


## -description


The 
<b>RtmGetLessSpecificDestination</b> function searches the routing table for a destination with the next-best-match (longest) prefix, given a destination prefix. The requested destination information is returned.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param DestHandle [in]

Handle to the destination.


### -param ProtocolId [in]

Specifies the protocol identifier. The <i>ProtocolID</i> is not part of the search criteria. The routing table manager uses this identifier to determine which route information to return. For example, if a client specifies the RIP protocol identifier, the best RIP route is returned, even if a non-RIP route is the best route to the destination. 




Specify RTM_BEST_PROTOCOL to return a route regardless of which protocol owns it. Specify RTM_THIS_PROTOCOL to return the best route for the calling protocol.


### -param TargetViews [in]

Specifies the views from which to return information. If the client specifies RTM_VIEW_MASK_ANY, destination information is returned from all views; however, no view-specific information is returned.


### -param DestInfo [out]

On input, <i>DestInfo</i> is a pointer to an 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure. 




On output, <i>DestInfo</i> is filled with the requested destination information.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The next best destination cannot be found.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The <i>DestInfo</i> parameter is a variable-sized 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure. If the client specifies more than one view using <i>TargetViews</i>, the size of <i>DestInfo</i> increases for each view. Use the 
<a href="https://msdn.microsoft.com/faad2b79-dcd0-47e7-95ab-05f6bad36650">RTM_SIZE_OF_DEST_INFO</a> macro to determine how much memory to allocate for the <i>DestInfo</i> structure before calling this function. Use the value specified for <i>TargetViews</i> as a parameter to 
<b>RTM_SIZE_OF_DEST_INFO</b>.

The 
<b>RtmGetLessSpecificDestination</b> function is used after a call to 
<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a> to return the next-best match for a destination. This call is also used after a prior call to 
<b>RtmGetLessSpecificDestination</b> to return the next successive less-specific match. Clients can use this function to "walk up" the prefix tree for a destination.

This call is also used after calls to functions that return an 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure, such as 
<a href="https://msdn.microsoft.com/bf6525ea-5f32-41d3-b436-920e7369b926">RtmGetDestInfo</a> and 
<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>.

The 
<b>RtmGetLessSpecificDestination</b> function returns matches until it reaches the default route, if it exists. Once the default route is found, 
<b>RtmGetLessSpecificDestination</b> returns ERROR_NOT_FOUND.

One common use for the 
<b>RtmGetLessSpecificDestination</b> and 
<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a> functions, is to retrieve each of the matching destinations.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/14e8e87f-c76c-48ad-93b5-0d8a711148d6">Search for Routes Using a Prefix Tree</a>.




## -see-also




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/0cbb24f4-30f4-41be-aea2-36474760d374">RtmGetExactMatchDestination</a>



<a href="https://msdn.microsoft.com/5fc9cde7-9912-409f-85ee-c775b4d6ddc0">RtmGetExactMatchRoute</a>



<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a>



<a href="https://msdn.microsoft.com/4c4b72a8-7a6c-4216-af2d-8dee55b910af">RtmIsBestRoute</a>
 

 

