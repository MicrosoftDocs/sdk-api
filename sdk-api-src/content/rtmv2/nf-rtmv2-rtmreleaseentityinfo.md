---
UID: NF:rtmv2.RtmReleaseEntityInfo
title: RtmReleaseEntityInfo function
author: windows-sdk-content
description: The RtmReleaseEntityInfo function releases a client structure.
old-location: rras\rtmreleaseentityinfo.htm
tech.root: rras
ms.assetid: ea72dde4-2d04-4ceb-b718-3ee96bf70464
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: RtmReleaseEntityInfo, RtmReleaseEntityInfo function [RAS], _rtmv2ref_rtmreleaseentityinfo, rras.rtmreleaseentityinfo, rtmv2/RtmReleaseEntityInfo
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
 - RtmReleaseEntityInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmReleaseEntityInfo function


## -description


The 
<b>RtmReleaseEntityInfo</b> function releases a client structure.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EntityInfo [in]

Pointer to the handle to release. The handle was obtained with a previous call to 
<a href="https://msdn.microsoft.com/6062369c-22c7-48e4-9dd3-91efba22df34">RtmGetEntityInfo</a>.


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




<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a>



<a href="https://msdn.microsoft.com/6062369c-22c7-48e4-9dd3-91efba22df34">RtmGetEntityInfo</a>
 

 

