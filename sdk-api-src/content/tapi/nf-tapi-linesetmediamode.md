---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# lineSetMediaMode function


## -description


The 
<b>lineSetMediaMode</b> function sets the media type(s) of the specified call in its 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure. For more information, see 
<a href="https://msdn.microsoft.com/627fe465-40f6-481e-9fd6-3fc3e2931e18">ITLegacyCallMediaControl::SetMediaType</a>.


## -parameters




### -param hCall

Handle to the call whose media type is to be changed. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


### -param dwMediaModes

New media type(s) for the call. This parameter uses the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>. As long as the UNKNOWN media type flag is set, other media type flags may be set as well. This is used to identify a call's media type as not fully determined, but narrowed down to one of a small set of specified media types. If the UNKNOWN flag is not set, only a single media type can be specified.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONUNAVAIL.




## -remarks



The 
<b>lineSetMediaMode</b> function changes the call's media type in its 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure. Typical usage of this operation is either to set a call's media type to a specific known media type or to exclude possible media types as long as the call's media type is officially unknown (the UNKNOWN media type flag is set).




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

