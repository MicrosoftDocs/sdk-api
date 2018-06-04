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

# CoordinateSpace enumeration


## -description


The <b>CoordinateSpace</b> enumeration specifies coordinate spaces. This enumeration is used by the 
			<a href="https://msdn.microsoft.com/d9c29b36-8f21-4d0b-99c7-5e7d635ee1a1">Graphics::TransformPoints</a> method, which converts points from one coordinate space to another. For more information about coordinate spaces, see <a href="https://msdn.microsoft.com/eb20f5e9-25f5-4f27-8ea5-83f6819425ed">Types of Coordinate Systems</a>. 


## -enum-fields




### -field CoordinateSpaceWorld

Specifies the world coordinate space. 


### -field CoordinateSpacePage

Specifies the page coordinate space. 


### -field CoordinateSpaceDevice

Specifies the device coordinate space. 


## -see-also




<a href="https://msdn.microsoft.com/d9c29b36-8f21-4d0b-99c7-5e7d635ee1a1">Graphics::TransformPoints</a>
 

 

