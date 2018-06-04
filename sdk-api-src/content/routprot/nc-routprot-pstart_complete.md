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

# PSTART_COMPLETE callback function


## -description


Router Manager calls the 
<b>StartComplete</b> function to inform the routing protocol that initialization is complete and all interfaces have been added. The routing protocol should wait for this call before starting any protocol-specific behavior.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PSTART_COMPLETE</a> type defines a pointer to this callback function. <i>StartComplete</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1








## -returns



This function should return NO_ERROR.




## -see-also




<a href="https://msdn.microsoft.com/8c1c0173-5abf-4e44-a633-16742fd2a4c0">StartProtocol</a>
 

 

