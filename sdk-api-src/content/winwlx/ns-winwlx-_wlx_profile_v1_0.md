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

# _WLX_PROFILE_V1_0 structure


## -description


<p class="CCE_Message">[The WLX_PROFILE_V1_0 structure is no longer available for use as of Windows Server 2008 and Windows Vista.]


			The <b>WLX_PROFILE_V1_0</b> structure contains information used for setting up the initial environment.


## -struct-fields




### -field dwType

Must be set to WLX_PROFILE_TYPE_V1_0.


### -field pszProfile

Pointer to the profile path (for example, "%SystemRoot%\system32\config\AprilM001"). 




The string pointed to by <b>pszProfile</b> must be separately allocated by your <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. It will be deallocated by <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a>.


## -remarks



The <b>WLX_PROFILE_V1_0</b> structure is returned to Winlogon by your GINA DLL following authentication. Winlogon uses the path specified by <b>pszProfile</b> to load the profile of the newly logged-on user.

GINA uses two structures to provide profile information: <a href="https://msdn.microsoft.com/6ecec95f-e663-4fb3-b2d4-82984f31cb62">WLX_PROFILE_V2_0</a> and <b>WLX_PROFILE_V1_0</b>. 




## -see-also




<a href="https://msdn.microsoft.com/6ecec95f-e663-4fb3-b2d4-82984f31cb62">WLX_PROFILE_V2_0</a>
 

 

