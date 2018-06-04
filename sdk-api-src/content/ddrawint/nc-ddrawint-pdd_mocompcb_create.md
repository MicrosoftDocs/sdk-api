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

# PDD_MOCOMPCB_CREATE callback function


## -description


The <i>DdMoCompCreate</i> callback function notifies the driver that a software decoder will start using motion compensation with the specified GUID. 


## -parameters




### -param Arg1








#### - lpCreateData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550529">DD_CREATEMOCOMPDATA</a> structure that contains the information required to begin using motion compensation.


## -returns



<i>DdMoCompCreate</i> returns one of the following callback codes:




## -remarks



<i>DdMoCompCreate</i> can be optionally implemented in DirectDraw drivers. It is not required for motion compensation support.

<i>DdMoCompCreate</i> also reports the width, height, and format of the output frame. The driver can fail this call if it cannot support motion compensation with these dimensions.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550529">DD_CREATEMOCOMPDATA</a>
 

 

