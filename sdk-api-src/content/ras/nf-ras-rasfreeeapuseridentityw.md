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

# RasFreeEapUserIdentityW function


## -description


Use the 
<b>RasFreeEapUserIdentity</b> function to free the memory buffer returned by 
<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a>.


## -parameters




### -param pRasEapUserIdentity [in]

Pointer to the 
<a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a> structure returned by the 
<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a> function. 
<b>RasFreeEapUserIdentity</b> frees the memory occupied by this structure.


## -returns



This function does not return a value.




## -remarks



<b>RasFreeEapUserIdentity</b> can be called with the <i>pRasEapUserIdentity</i> parameter equal to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a>



<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a>
 

 

