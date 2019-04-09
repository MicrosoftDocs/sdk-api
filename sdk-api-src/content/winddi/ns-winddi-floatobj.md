---
UID: NS:winddi._FLOATOBJ
title: FLOATOBJ (winddi.h)
author: windows-sdk-content
description: The FLOATOBJ structure is used to emulate a floating-point number.
old-location: display\floatobj.htm
tech.root: display
ms.assetid: 5f8c401b-7487-4d75-a0a8-534fa7992a3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFLOATOBJ, FLOATOBJ, FLOATOBJ structure [Display Devices], PFLOATOBJ, PFLOATOBJ structure pointer [Display Devices], display.floatobj, grstrcts_5e2796fc-6ccc-4230-9ded-fd2222f0e8ac.xml, winddi/FLOATOBJ, winddi/PFLOATOBJ"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: FLOATOBJ, *PFLOATOBJ
req.redist: 
---

# FLOATOBJ structure


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




<a href="https://msdn.microsoft.com/6502d863-ab3e-46d2-8da4-c2f1b01fe344">FLOATOBJ_Add</a>



<a href="https://msdn.microsoft.com/47af86ec-a7b2-49c1-aeda-1a273f17c4ae">FLOATOBJ_AddFloat</a>



<a href="https://msdn.microsoft.com/a6355e47-5373-4b03-bafc-308a64e8e0aa">FLOATOBJ_AddLong</a>



<a href="https://msdn.microsoft.com/110473d8-712a-4670-96e0-daf57dd5efd2">FLOATOBJ_Div</a>



<a href="https://msdn.microsoft.com/47ebf68c-6dfa-43d3-8bc9-1f0b8f030974">FLOATOBJ_DivFloat</a>



<a href="https://msdn.microsoft.com/23452749-1a10-4d19-b24a-24ec42931efd">FLOATOBJ_DivLong</a>



<a href="https://msdn.microsoft.com/1fc9afcb-7b65-415c-ae6c-8885ef47abe9">FLOATOBJ_Equal</a>



<a href="https://msdn.microsoft.com/ab81a183-6517-4353-accb-425f02004577">FLOATOBJ_EqualLong</a>



<a href="https://msdn.microsoft.com/1deddee5-c987-45b0-bb0f-ff4f766fdde0">FLOATOBJ_GetFloat</a>



<a href="https://msdn.microsoft.com/e3f4355f-c716-4757-9f82-d4f109e05845">FLOATOBJ_GetLong</a>



<a href="https://msdn.microsoft.com/45e743e4-a72d-413a-9ee3-79eab517c87e">FLOATOBJ_GreaterThan</a>



<a href="https://msdn.microsoft.com/2d464472-c89b-47ad-811e-a2f5445e12a9">FLOATOBJ_GreaterThanLong</a>



<a href="https://msdn.microsoft.com/acd1cc6d-c88f-4336-8a6c-a8b02cf726ee">FLOATOBJ_LessThan</a>



<a href="https://msdn.microsoft.com/10665f5d-68ae-4f72-9fa2-c79cf86ded3d">FLOATOBJ_LessThanLong</a>



<a href="https://msdn.microsoft.com/95b4c3eb-5e62-4209-9c05-eae9ab48f7ab">FLOATOBJ_Mul</a>



<a href="https://msdn.microsoft.com/7b4189f7-b80b-4543-b713-b0b2d06ef81e">FLOATOBJ_MulFloat</a>



<a href="https://msdn.microsoft.com/945b9280-41fc-44f9-a5df-c0a725cef377">FLOATOBJ_MulLong</a>



<a href="https://msdn.microsoft.com/08a4c47f-8bf5-4849-8ce9-e5999c02f263">FLOATOBJ_Neg</a>



<a href="https://msdn.microsoft.com/ba2c33fa-9489-482d-b27e-79537425cc4b">FLOATOBJ_SetFloat</a>



<a href="https://msdn.microsoft.com/4fa1b8a6-8172-4047-9ee2-fe00f0924487">FLOATOBJ_SetLong</a>



<a href="https://msdn.microsoft.com/0ba6edfa-2de6-4eaa-8853-0e20c01cedf8">FLOATOBJ_Sub</a>



<a href="https://msdn.microsoft.com/0fa69283-3236-43bc-9c16-6bd220ad4e0c">FLOATOBJ_SubFloat</a>



<a href="https://msdn.microsoft.com/2a3e8a17-3718-4212-adfe-f109e286bec6">FLOATOBJ_SubLong</a>



<a href="https://msdn.microsoft.com/0c58a0df-4a0a-46e2-90de-dc50b8077709">FLOATOBJ_XFORM</a>



<a href="https://msdn.microsoft.com/761c6061-841b-4187-a826-575d2a5086db">XFORMOBJ_iGetFloatObjXform</a>
 

 

