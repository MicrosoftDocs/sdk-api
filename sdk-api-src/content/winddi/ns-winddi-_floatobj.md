---
UID: NS:winddi._FLOATOBJ
title: "_FLOATOBJ"
author: windows-sdk-content
description: The FLOATOBJ structure is used to emulate a floating-point number.
old-location: display\floatobj.htm
old-project: display
ms.assetid: 5f8c401b-7487-4d75-a0a8-534fa7992a3d
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: "*PFLOATOBJ, FLOATOBJ, FLOATOBJ structure [Display Devices], PFLOATOBJ, PFLOATOBJ structure pointer [Display Devices], _FLOATOBJ, display.floatobj, grstrcts_5e2796fc-6ccc-4230-9ded-fd2222f0e8ac.xml, winddi/FLOATOBJ, winddi/PFLOATOBJ"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
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
tech.root: 
req.typenames: FLOATOBJ, *PFLOATOBJ
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FLOATOBJ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

