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

# D3D10_COLOR_WRITE_ENABLE enumeration


## -description


Identify which components of each pixel of a render target are writable during <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">blending</a>.


## -enum-fields




### -field D3D10_COLOR_WRITE_ENABLE_RED

Allow data to be stored in the red component.


### -field D3D10_COLOR_WRITE_ENABLE_GREEN

Allow data to be stored in the green component.


### -field D3D10_COLOR_WRITE_ENABLE_BLUE

Allow data to be stored in the blue component.


### -field D3D10_COLOR_WRITE_ENABLE_ALPHA

Allow data to be stored in the alpha component.


### -field D3D10_COLOR_WRITE_ENABLE_ALL

Allow data to be stored in all components.


## -remarks



These flags can be combined with a bitwise OR.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

