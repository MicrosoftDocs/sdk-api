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

# PDD_MOCOMPCB_GETINTERNALINFO callback function


## -description


The <b>DdMoCompGetInternalInfo</b> callback function allows the driver to report that it internally allocates display memory to perform motion compensation. 


## -parameters




### -param Arg1








#### - lpInternalData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551574">DD_GETINTERNALMOCOMPDATA</a> structure that contains the internal memory requirements.


## -returns



<b>DdMoCompGetInternalInfo</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompGetInternalInfo</b>.

This function allows the decoder and DirectShow to make better-informed decisions regarding what GUID to choose.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551574">DD_GETINTERNALMOCOMPDATA</a>
 

 

