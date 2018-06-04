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

# DsGetSiteNameA function


## -description


The <b>DsGetSiteName</b> function returns the name of the site where a computer resides. For a domain controller (DC), the name of the site is the location of the configured DC. For a member workstation or member server, the name specifies the workstation site as configured in the domain of the computer.


## -parameters




### -param OPTIONAL

TBD


### -param SiteName [out]

Pointer to a variable that receives a pointer to a null-terminated string specifying the site location of this computer. This string is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


#### - ComputerName [in]

Pointer to a null-terminated string that specifies the name of the server to send this function. A <b>NULL</b> implies the local computer.


## -returns



If the function returns account information, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.




## -remarks



The <b>DsGetSiteName</b> function does not require any particular access to the specified domain. The function is sent to the "NetLogon" service on the computer specified by <i>ComputerName</i>.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/bed49e08-4cb7-439c-bfb7-815263ec7568">DsValidateSubnetName</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>
 

 

