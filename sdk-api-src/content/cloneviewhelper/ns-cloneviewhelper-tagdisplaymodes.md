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

# tagDisplayModes structure


## -description


The DisplayModes structure contains a list of display modes. 


## -struct-fields




### -field numDisplayModes

The number of display modes in the array that the <b>displayMode</b> member specifies. 


### -field displayMode

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff554037">DisplayMode</a> structures that describe characteristics of display devices. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff554037">DisplayMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568176">IViewHelper::SetConfiguration</a>
 

 

