---
UID: NF:rtmv2.RtmReleaseEntities
title: RtmReleaseEntities function
author: windows-sdk-content
description: The RtmReleaseEntities function releases the client handles returned by RtmGetRegisteredEntities.
old-location: rras\rtmreleaseentities.htm
tech.root: RRAS
ms.assetid: 1f6c4275-0129-4f27-b9b2-bfda33d34d21
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RtmReleaseEntities, RtmReleaseEntities function [RAS], _rtmv2ref_rtmreleaseentities, rras.rtmreleaseentities, rtmv2/RtmReleaseEntities
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
 - RtmReleaseEntities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtmReleaseEntities
: 
---

# RtmReleaseEntities function


## -description


The 
<b>RtmReleaseEntities</b> function releases the client handles returned by 
<a href="https://msdn.microsoft.com/411e15bc-7f47-4ef7-9400-292203b581af">RtmGetRegisteredEntities</a>.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NumEntities [in]

Specifies the number of clients in <i>EntityHandles</i>.


### -param EntityHandles [in]

Pointer to an array of client handles to release. The handles were obtained from a previous call to 
<a href="https://msdn.microsoft.com/411e15bc-7f47-4ef7-9400-292203b581af">RtmGetRegisteredEntities</a>.


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




<a href="https://msdn.microsoft.com/411e15bc-7f47-4ef7-9400-292203b581af">RtmGetRegisteredEntities</a>
 

 

