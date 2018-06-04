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

# tagAdapter structure


## -description


The Adapter structure describes a graphics adapter. 


## -struct-fields




### -field AdapterName

A single wide-character string that holds the name of the graphics adapter. 


### -field numSources

The number of video present sources in the array that the <b>sources</b> member specifies. 


### -field sources

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569715">Sources</a> structures that specify a list of Video Present Network (VidPN) topologies. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568176">IViewHelper::SetConfiguration</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569715">Sources</a>
 

 

