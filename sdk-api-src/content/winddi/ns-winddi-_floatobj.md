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

# _FLOATOBJ structure


## -description


The FLOATOBJ structure is used to emulate a floating-point number.


## -struct-fields




### -field ul1

Reserved for system use.


### -field ul2

Reserved for system use.


## -remarks



This structure, in conjunction with the <b>FLOATOBJ_</b><i>Xxx</i> service routines, allows graphics drivers to emulate floating-point arithmetic in the NT kernel. Floating-point arithmetic is not otherwise supported in the NT kernel code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565814">FLOATOBJ_Add</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565822">FLOATOBJ_AddFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565826">FLOATOBJ_AddLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565835">FLOATOBJ_Div</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565841">FLOATOBJ_DivFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565845">FLOATOBJ_DivLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565861">FLOATOBJ_Equal</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565870">FLOATOBJ_EqualLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565871">FLOATOBJ_GetFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565873">FLOATOBJ_GetLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565880">FLOATOBJ_GreaterThan</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565884">FLOATOBJ_GreaterThanLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565894">FLOATOBJ_LessThan</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565902">FLOATOBJ_LessThanLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565908">FLOATOBJ_Mul</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565914">FLOATOBJ_MulFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565916">FLOATOBJ_MulLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565919">FLOATOBJ_Neg</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565922">FLOATOBJ_SetFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565928">FLOATOBJ_SetLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565935">FLOATOBJ_Sub</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565938">FLOATOBJ_SubFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565941">FLOATOBJ_SubLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565950">FLOATOBJ_XFORM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570627">XFORMOBJ_iGetFloatObjXform</a>
 

 

