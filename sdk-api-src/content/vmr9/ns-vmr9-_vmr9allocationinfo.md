---
UID: NS:vmr9._VMR9AllocationInfo
title: "_VMR9AllocationInfo"
author: windows-sdk-content
description: The VMR9AllocationInfo structure describes the Direct3D surfaces that a VMR-9 Allocator-Presenter object should allocate.
old-location: dshow\vmr9allocationinfo.htm
tech.root: DirectShow
ms.assetid: d263b004-30e6-4dff-9df2-f4ca492f09f7
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: VMR9AllocationInfo, VMR9AllocationInfo structure [DirectShow], VMR9AllocationInfoStructure, _VMR9AllocationInfo, dshow.vmr9allocationinfo, vmr9/VMR9AllocationInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9AllocationInfo
product: Windows
targetos: Windows
req.typenames: VMR9AllocationInfo
req.redist: 
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
 

 

