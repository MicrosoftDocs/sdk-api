---
UID: NS:strmif.tagVMRALLOCATIONINFO
title: tagVMRALLOCATIONINFO
author: windows-sdk-content
description: The VMRALLOCATIONINFO structure is used in the VMR-7 filter's IVMRSurfaceAllocator::AllocateSurface method.
old-location: dshow\vmrallocationinfo.htm
tech.root: DirectShow
ms.assetid: 3908f9d1-5120-413b-a142-08cd9005c401
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: VMRALLOCATIONINFO, VMRALLOCATIONINFO structure [DirectShow], VMRALLOCATIONINFOStructure, dshow.vmrallocationinfo, strmif/VMRALLOCATIONINFO, tagVMRALLOCATIONINFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
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
 - strmif.h
api_name:
 - VMRALLOCATIONINFO
product: Windows
targetos: Windows
req.typenames: VMRALLOCATIONINFO
req.redist: 
req.product: Windows XP
---

# tagVMRALLOCATIONINFO structure


## -description



The <code>VMRALLOCATIONINFO</code> structure is used in the VMR-7 filter's <a href="https://msdn.microsoft.com/6783df91-c92f-45d0-b299-16cdbc4bb630">IVMRSurfaceAllocator::AllocateSurface</a> method.




## -struct-fields




### -field dwFlags

A bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/1f75b357-0ce0-4efe-b1a8-39200e6b3d1a">VMRSurfaceAllocationFlags</a> enumeration.
          


### -field lpHdr

Pointer to the <b>BITMAPINFOHEADER</b> structure associated with the surface.


### -field lpPixFmt

Pointer to the <b>DDPIXELFORMAT</b> structure associated with the surface.


### -field szAspectRatio

A <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that specifies the aspect ratio of the new surface.


### -field dwMinBuffers

The minimum number of buffers to create for this surface.


### -field dwMaxBuffers

The maximum number of buffers to create for this surface.
          


### -field dwInterlaceFlags

A bitwise <b>OR</b> of  flags that indicate the interlacing. For a list of flags, see the <b>dwInterlaceFlags</b> member of the <a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2</a> structure.
          


### -field szNativeSize

The size of the native video rectangle.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

