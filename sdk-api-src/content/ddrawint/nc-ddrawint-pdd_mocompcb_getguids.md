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

# PDD_MOCOMPCB_GETGUIDS callback function


## -description


The <b>DdMoCompGetGuids</b> callback function retrieves the number of GUIDs the driver supports.


## -parameters




### -param Arg1








#### - lpGetGuidData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551587">DD_GETMOCOMPGUIDSDATA</a> structure that contains the GUID information.


## -returns



<b>DdMoCompGetGuids</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompGetGuids</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551587">DD_GETMOCOMPGUIDSDATA</a>
 

 

