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

# PRESUTIL_START_RESOURCE_SERVICE callback function


## -description


Starts a <a href="https://msdn.microsoft.com/library/windows/hardware/mt269769">service</a>. The <b>PRESUTIL_START_RESOURCE_SERVICE</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to start.


### -param phServiceHandle [out]

Optional pointer to a handle in which the handle to the started service is returned. This handle must be closed either by a call to the cluster utility function  <a href="https://msdn.microsoft.com/22be9285-7db6-43dc-bf41-08187bbefc41">ResUtilStopService</a> or the function  <a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -remarks



The  <i>ResUtilStartResourceService</i> utility function encapsulates the necessary calls to the service control manager, providing a convenient way to start services in the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. Using  <i>ResUtilStartResourceService</i> is optional. If the service to be started requires specific access restrictions or other special handling, use the service control manager functions instead.




## -see-also




<a href="https://msdn.microsoft.com/22be9285-7db6-43dc-bf41-08187bbefc41">ResUtilStopService</a>
 

 

