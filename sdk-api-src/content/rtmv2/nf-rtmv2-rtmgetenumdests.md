---
UID: NF:rtmv2.RtmGetEnumDests
title: RtmGetEnumDests function (rtmv2.h)
author: windows-sdk-content
description: The RtmGetEnumDests function retrieves the next set of destinations in the specified enumeration.
old-location: rras\rtmgetenumdests.htm
tech.root: RRAS
ms.assetid: f793b54e-9591-4b9f-b109-8487013c7af5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmGetEnumDests, RtmGetEnumDests function [RAS], _rtmv2ref_rtmgetenumdests, rras.rtmgetenumdests, rtmv2/RtmGetEnumDests
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
 - RtmGetEnumDests
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtmGetEnumDests function


## -description


The 
<b>RtmGetEnumDests</b> function retrieves the next set of destinations in the specified enumeration.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EnumHandle [in]

Handle to the destination enumeration.


### -param NumDests [in, out]

On input, <i>NumDests</i> is a pointer to a <b>UINT</b> value specifying the maximum number of destinations that can be received by <i>DestInfos</i>. On output, <i>NumDests</i> receives the actual number of destinations received by <i>DestInfos</i>.


### -param DestInfos [out]

On input, <i>DestInfos</i> is a pointer to an 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure. 




On output, <i>DestInfos</i> receives an array of handles to destinations.


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
The value pointed to by <i>NumRoutes</i> is larger than the maximum number of routes a client is allowed to retrieve with one call. Check 
<a href="https://msdn.microsoft.com/26644a09-8d49-4c9f-a7cd-5edbf93e83d0">RTM_REGN_PROFILE</a> for the maximum number of destinations that the client is allowed to retrieve with one call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more destinations to enumerate.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The structure pointed to by <i>DestInfos</i>  is a variable-sized structure. If the client specifies more than one view with <i>TargetViews</i>, the size of <i>DestInfos</i> increases for each view. Use the 
<a href="https://msdn.microsoft.com/faad2b79-dcd0-47e7-95ab-05f6bad36650">RTM_SIZE_OF_DEST_INFO</a> macro to determine how large a <i>DestInfos</i> structure to allocate before calling this function. Use the value specified for <i>TargetViews</i> as a parameter to 
<b>RTM_SIZE_OF_DEST_INFO</b>.

When the destinations are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/eb338b7f-8461-4980-b92f-09d976661ff2">RtmReleaseDests</a>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/0dced1f8-5dc3-4233-aeb9-35c81c34b345">Enumerate All Destinations</a>.




## -see-also




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/6efea7b4-dd44-4b08-999d-62e7f660ed64">RtmCreateDestEnum</a>



<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>



<a href="https://msdn.microsoft.com/eb338b7f-8461-4980-b92f-09d976661ff2">RtmReleaseDests</a>
 

 

