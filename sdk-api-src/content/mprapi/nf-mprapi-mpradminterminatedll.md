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

# MprAdminTerminateDll function


## -description


When the RAS shuts down, it calls the 
<b>MprAdminTerminateDll</b> function exported by the administration DLL. Use this function to perform any required clean-up for the DLL.


## -parameters






## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.




## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of <a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a> in the order in which the DLLs are listed in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926940">registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

