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

# PDD_MOCOMPCB_DESTROY callback function


## -description


The <b>DdMoCompDestroy</b> callback function notifies the driver that this motion compensation object will no longer be used. The driver now needs to perform any necessary cleanup.


## -parameters




### -param Arg1








#### - lpDestroyData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550570">DD_DESTROYMOCOMPDATA</a> structure that contains the information needed to finish motion compensation.


## -returns



<b>DdMoCompDestroy</b> returns one of the following callback codes:




## -remarks



<b>DdMoCompDestroy</b> can be optionally implemented in DirectDraw drivers. It is not required for motion compensation support.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550570">DD_DESTROYMOCOMPDATA</a>
 

 

