---
UID: NS:vmr9._VMR9NormalizedRect
title: "_VMR9NormalizedRect"
author: windows-sdk-content
description: The VMR9NormalizedRect structure is used with the VMR-9 filter in mixing operations to specify or retrieve the location of a video rectangle in composition space.
old-location: dshow\vmr9normalizedrect.htm
tech.root: DirectShow
ms.assetid: 226b685c-92da-45c3-b99a-6c1e732f8dc6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: VMR9NormalizedRect, VMR9NormalizedRect structure [DirectShow], VMR9NormalizedRectStructure, _VMR9NormalizedRect, dshow.vmr9normalizedrect, vmr9/VMR9NormalizedRect
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - VMR9NormalizedRect
product: Windows
targetos: Windows
req.typenames: VMR9NormalizedRect
req.redist: 
---

# _VMR9NormalizedRect structure


## -description



The <code>VMR9NormalizedRect</code> structure is used with the VMR-9 filter in mixing operations to specify or retrieve the location of a video rectangle in composition space.




## -struct-fields




### -field left

Specifies left.


### -field top

Specifies top.


### -field right

Specifies right.


### -field bottom

Specifies bottom.


## -remarks



This structure is used in methods involving "composition space," which refers to the visible video rectangle, as well as the "offscreen" space necessary to contain rectangles from secondary streams. See <a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

