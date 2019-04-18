---
UID: NS:vmr9._VMR9AllocationInfo
title: VMR9AllocationInfo (vmr9.h)
author: windows-sdk-content
description: The VMR9AllocationInfo structure describes the Direct3D surfaces that a VMR-9 Allocator-Presenter object should allocate.
old-location: dshow\vmr9allocationinfo.htm
tech.root: DirectShow
ms.assetid: d263b004-30e6-4dff-9df2-f4ca492f09f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VMR9AllocationInfo, VMR9AllocationInfo structure [DirectShow], VMR9AllocationInfoStructure, dshow.vmr9allocationinfo, vmr9/VMR9AllocationInfo
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
ms.custom: 19H1
---

# VMR9AllocationInfo structure


## -description



The <b>VMR9AllocationInfo</b> structure describes the Direct3D surfaces that a VMR-9 Allocator-Presenter object should allocate.




## -struct-fields




### -field dwFlags

Specifies a bitwise combination of flags from the <a href="https://msdn.microsoft.com/en-us/library/Dd407376(v=VS.85).aspx">VMR9SurfaceAllocationFlags</a> enumeration type.


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



<a href="https://msdn.microsoft.com/en-us/library/Dd390503(v=VS.85).aspx">IVMRSurfaceAllocator9::InitializeDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390510(v=VS.85).aspx">IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper</a>
 

 

