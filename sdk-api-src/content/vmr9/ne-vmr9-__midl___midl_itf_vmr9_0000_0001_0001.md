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

# __MIDL___MIDL_itf_vmr9_0000_0001_0001 enumeration


## -description



The <b>VMR9SurfaceAllocationFlags</b> enumeration type is used with the <a href="https://msdn.microsoft.com/44c22dc0-98a9-4a6e-a488-1d70dfff6acd">IVMRSurfaceAllocator9::InitializeDevice</a> method to specify surface creation parameters (VMR-9 only).




## -enum-fields




### -field VMR9AllocFlag_3DRenderTarget

Indicates that the surface is a Direct3D render target.


### -field VMR9AllocFlag_DXVATarget

Indicates that the render target supports DXVA.


### -field VMR9AllocFlag_TextureSurface

Indicates that the target is a Direct3D texture surface.


### -field VMR9AllocFlag_OffscreenSurface

Indicates an offscreen surface.


### -field VMR9AllocFlag_RGBDynamicSwitch

In YUV mixing mode, indicates that the mixer can accept RGB formats in addition to the specified YUV format. The allocator-presenter can switch between the formats dynamically. This flag is only valid in YUV mixing mode.


### -field VMR9AllocFlag_UsageReserved

Reserved for future use.


### -field VMR9AllocFlag_UsageMask

Bitwise <b>OR</b> of all flags; not used by applications


## -remarks



The VMR9AllocFlag_TextureSurface flag can be combined with the VMR9AllocFlag_DXVATarget and VMR9AllocFlag_3DRenderTarget flags.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

