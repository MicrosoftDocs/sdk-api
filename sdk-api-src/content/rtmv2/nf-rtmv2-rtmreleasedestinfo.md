---
UID: NF:rtmv2.RtmReleaseDestInfo
title: RtmReleaseDestInfo function
author: windows-sdk-content
description: The RtmReleaseDestInfo function releases a destination structure.
old-location: rras\rtmreleasedestinfo.htm
tech.root: RRAS
ms.assetid: 43992abd-7e52-4d1b-b693-f437f5ba77cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmReleaseDestInfo, RtmReleaseDestInfo function [RAS], _rtmv2ref_rtmreleasedestinfo, rras.rtmreleasedestinfo, rtmv2/RtmReleaseDestInfo
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
 - RtmReleaseDestInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmReleaseDestInfo function


## -description


The 
<b>RtmReleaseDestInfo</b> function releases a destination structure.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param DestInfo [in]

Pointer to the destination to release. The destination was obtained from a previous call to a function that returns an 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure.


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




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/bf6525ea-5f32-41d3-b436-920e7369b926">RtmGetDestInfo</a>
 

 

