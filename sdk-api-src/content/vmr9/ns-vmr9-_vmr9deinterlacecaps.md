---
UID: NS:vmr9._VMR9DeinterlaceCaps
title: "_VMR9DeinterlaceCaps"
author: windows-sdk-content
description: The VMR9DeinterlaceCaps structure describes the capabilities of a deinterlacing mode.
old-location: dshow\vmr9deinterlacecaps.htm
tech.root: DirectShow
ms.assetid: ae71c9d6-2540-4679-927c-e1d759df7009
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: VMR9DeinterlaceCaps, VMR9DeinterlaceCaps structure [DirectShow], VMR9DeinterlaceCapsStructure, _VMR9DeinterlaceCaps, dshow.vmr9deinterlacecaps, vmr9/VMR9DeinterlaceCaps
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
 - VMR9DeinterlaceCaps
product: Windows
targetos: Windows
req.typenames: VMR9DeinterlaceCaps
req.redist: 
---

# _VMR9DeinterlaceCaps structure


## -description



The <code>VMR9DeinterlaceCaps</code> structure describes the capabilities of a deinterlacing mode.




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

Bitwise combination of flags from the <a href="https://msdn.microsoft.com/2b0b56b7-bab3-4184-a453-2da880aa38c9">VMR9DeinterlaceTech</a> enumeration type. These flags are used to describe the deinterlacing algorithm.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

