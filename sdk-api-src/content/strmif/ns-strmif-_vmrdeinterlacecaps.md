---
UID: NS:strmif._VMRDeinterlaceCaps
title: "_VMRDeinterlaceCaps"
author: windows-sdk-content
description: The VMRDeinterlaceCaps structure describes the capabilities of a deinterlacing mode.
old-location: dshow\vmrdeinterlacecaps.htm
tech.root: DirectShow
ms.assetid: e6152130-d574-4c9e-9d35-a42de709f9ae
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: VMRDeinterlaceCaps, VMRDeinterlaceCaps structure [DirectShow], VMRDeinterlaceCapsStructure, _VMRDeinterlaceCaps, dshow.vmrdeinterlacecaps, strmif/VMRDeinterlaceCaps
ms.prod: windows
ms.technology: windows-sdk
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
 - VMRDeinterlaceCaps
product: Windows
targetos: Windows
req.typenames: VMRDeinterlaceCaps
req.redist: 
req.product: Windows XP with SP1 and later
---

# _VMRDeinterlaceCaps structure


## -description



The <code>VMRDeinterlaceCaps</code> structure describes the capabilities of a deinterlacing mode.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwNumPreviousOutputFrames

Number of previously de-interlaced frames that must be fed back to the hardware to deinterlace the next field. (Used by recursive deinterlacing algorithms.)


### -field dwNumForwardRefSamples

Number of future samples needed to deinterlace the current field.


### -field dwNumBackwardRefSamples

Number of past samples needed to deinterlace the current field.


### -field DeinterlaceTechnology

Bitwise combination of flags from the <a href="https://msdn.microsoft.com/10149023-c5e8-4dce-8a8c-cde96ae6c073">VMRDeinterlaceTech</a> enumeration type. These flags are used to describe the deinterlacing algorithm.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>
 

 

