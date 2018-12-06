---
UID: NF:rtmv2.RtmGetDestInfo
title: RtmGetDestInfo function
author: windows-sdk-content
description: The RtmGetDestInfo function returns information about a destination.
old-location: rras\rtmgetdestinfo.htm
tech.root: rras
ms.assetid: bf6525ea-5f32-41d3-b436-920e7369b926
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmGetDestInfo, RtmGetDestInfo function [RAS], _rtmv2ref_rtmgetdestinfo, rras.rtmgetdestinfo, rtmv2/RtmGetDestInfo
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
 - RtmGetDestInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmGetDestInfo function


## -description


The 
<b>RtmGetDestInfo</b> function returns information about a destination.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param DestHandle [in]

Handle to the destination for which to return information.


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



The  structure pointed to by <i>DestInfo</i> is a variable-sized structure. If the client specifies more than one view with <i>TargetViews</i>, the size of <i>DestInfo</i> increases for each view. Use the 
<a href="https://msdn.microsoft.com/faad2b79-dcd0-47e7-95ab-05f6bad36650">RTM_SIZE_OF_DEST_INFO</a> macro to determine how large a <i>DestInfo</i> structure to allocate before calling this function. Use the value specified for <i>TargetViews</i> as a parameter to 
<b>RTM_SIZE_OF_DEST_INFO</b>.

Use 
<a href="https://msdn.microsoft.com/43992abd-7e52-4d1b-b693-f437f5ba77cb">RtmReleaseDestInfo</a> to release the <i>DestInfo</i> buffer.




## -see-also




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/43992abd-7e52-4d1b-b693-f437f5ba77cb">RtmReleaseDestInfo</a>
 

 

