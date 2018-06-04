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

# D2D1_RENDER_TARGET_USAGE enumeration


## -description



    Describes how a render target is remoted and whether it should be GDI-compatible. This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_RENDER_TARGET_USAGE_NONE

The render target attempts to use Direct3D command-stream remoting and uses bitmap remoting if stream remoting fails. The render target is not GDI-compatible.


### -field D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING

The render target renders content locally and sends it to the terminal services client as a bitmap. 


### -field D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE

The render target can be used efficiently with GDI.


### -field D2D1_RENDER_TARGET_USAGE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>
 

 

