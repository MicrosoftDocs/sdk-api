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

# _VMR9AllocationInfo structure


## -description



The <b>VMR9AllocationInfo</b> structure describes the Direct3D surfaces that a VMR-9 Allocator-Presenter object should allocate.




## -struct-fields




### -field dwFlags

Specifies a bitwise combination of flags from the <a href="https://msdn.microsoft.com/880e6c78-177f-49d0-a526-5f036c715f9e">VMR9SurfaceAllocationFlags</a> enumeration type.


### -field dwWidth

Specifies the width of the surfaces.


### -field dwHeight

Specifies the height of the surfaces.


### -field Format

Specifies the surface format, as a <b>D3DFORMAT</b> type. The value D3DFMT_UNKNOWN (zero) indicates that the surface format should be compatible with the display.


### -field Pool

Specifies the Direct3D memory pool to use for the surfaces, as a <b>D3DPOOL</b> type.


### -field MinBuffers

Specifies the minimum number of buffers to create.


### -field szAspectRatio

Specifies the video aspect ratio as a <b>SIZE</b> structure.


### -field szNativeSize

Specifies the native video size as a <b>SIZE</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/44c22dc0-98a9-4a6e-a488-1d70dfff6acd">IVMRSurfaceAllocator9::InitializeDevice</a>



<a href="https://msdn.microsoft.com/b69db9e9-6ab0-40ad-b929-30613c0b9e4b">IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper</a>
 

 

