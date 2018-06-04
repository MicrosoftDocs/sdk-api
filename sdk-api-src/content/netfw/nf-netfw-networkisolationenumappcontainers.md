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

# NetworkIsolationEnumAppContainers function


## -description


The <b>NetworkIsolationEnumAppContainers</b> function enumerates all of the app containers that have been created in the system.


## -parameters




### -param Flags [in]

Type: <b>DWORD</b>

May be set to <b>NETISO_FLAG_FORCE_COMPUTE_BINARIES</b> to ensure that all binaries are computed before the app container is returned. This flag should be set if the caller requires up-to-date and complete information on app container binaries. If this flag is not set, returned data may be stale or incomplete.


See <a href="https://msdn.microsoft.com/0e07c3ed-0561-453d-b92a-cd0db07ea5cf">NETISO_FLAG</a> for more information.


### -param pdwNumPublicAppCs [out]

Type: <b>DWORD*</b>

The number of app containers in the <b>ppPublicAppCs</b> member.


### -param ppPublicAppCs [out]

Type: <b><a href="https://msdn.microsoft.com/0567fb66-0511-4c80-9e31-2412507ced97">PINET_FIREWALL_APP_CONTAINER</a>*</b>

The list of app container structure elements.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 

ERROR_OUTOFMEMORY will be returned if memory is unavailable.




## -remarks



If no app containers are installed on the system, ERROR_SUCCESS will still be returned (and <i>ppPublicAppCs</i> will be empty).




## -see-also




<a href="https://msdn.microsoft.com/0567fb66-0511-4c80-9e31-2412507ced97">INET_FIREWALL_APP_CONTAINER</a>



<a href="https://msdn.microsoft.com/0e07c3ed-0561-453d-b92a-cd0db07ea5cf">NETISO_FLAG</a>
 

 

