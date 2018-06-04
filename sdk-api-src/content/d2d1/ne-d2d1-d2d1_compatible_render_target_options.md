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

# D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS enumeration


## -description


Specifies additional features supportable by a compatible render target when it is created. 
    This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE

The render target supports no additional features.


### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE

The render target supports interoperability with the Windows Graphics Device Interface  (GDI). 


### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_FORCE_DWORD




## -remarks



Use this enumeration when creating a compatible render target with the <a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a> method. For more information about compatible render targets, see the <a href="https://msdn.microsoft.com/8a67babd-20c7-47f4-8dd3-8c0320d89ad6">Render Targets Overview</a>. 

The <b>D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE</b> option may only be requested if the parent render target was created with <a href="https://msdn.microsoft.com/12d717c4-5f81-4bbf-a693-042e51913081">D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE</a> (for most render targets) or <b>D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE</b> (for render targets created by the <a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a> method).




## -see-also




<a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a>



<a href="https://msdn.microsoft.com/8a67babd-20c7-47f4-8dd3-8c0320d89ad6">Render Targets Overview</a>
 

 

