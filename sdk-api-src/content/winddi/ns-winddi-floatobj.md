---
UID: NS:winddi._FLOATOBJ
title: FLOATOBJ (winddi.h)
description: The FLOATOBJ structure is used to emulate a floating-point number.
helpviewer_keywords: ["*PFLOATOBJ","FLOATOBJ","FLOATOBJ structure [Display Devices]","PFLOATOBJ","PFLOATOBJ structure pointer [Display Devices]","display.floatobj","grstrcts_5e2796fc-6ccc-4230-9ded-fd2222f0e8ac.xml","winddi/FLOATOBJ","winddi/PFLOATOBJ"]
old-location: display\floatobj.htm
tech.root: display
ms.assetid: 5f8c401b-7487-4d75-a0a8-534fa7992a3d
ms.date: 12/05/2018
ms.keywords: '*PFLOATOBJ, FLOATOBJ, FLOATOBJ structure [Display Devices], PFLOATOBJ, PFLOATOBJ structure pointer [Display Devices], display.floatobj, grstrcts_5e2796fc-6ccc-4230-9ded-fd2222f0e8ac.xml, winddi/FLOATOBJ, winddi/PFLOATOBJ'
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
targetos: Windows
req.typenames: FLOATOBJ, *PFLOATOBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FLOATOBJ
 - winddi/_FLOATOBJ
 - PFLOATOBJ
 - winddi/PFLOATOBJ
 - FLOATOBJ
 - winddi/FLOATOBJ
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FLOATOBJ
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

<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_add">FLOATOBJ_Add</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_addfloat">FLOATOBJ_AddFloat</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_addlong">FLOATOBJ_AddLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_div">FLOATOBJ_Div</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_divfloat">FLOATOBJ_DivFloat</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_divlong">FLOATOBJ_DivLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_equal">FLOATOBJ_Equal</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_equallong">FLOATOBJ_EqualLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_getfloat">FLOATOBJ_GetFloat</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_getlong">FLOATOBJ_GetLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_greaterthan">FLOATOBJ_GreaterThan</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_greaterthanlong">FLOATOBJ_GreaterThanLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_lessthan">FLOATOBJ_LessThan</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_lessthanlong">FLOATOBJ_LessThanLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_mul">FLOATOBJ_Mul</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_mulfloat">FLOATOBJ_MulFloat</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_mullong">FLOATOBJ_MulLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_neg">FLOATOBJ_Neg</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_setfloat">FLOATOBJ_SetFloat</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_setlong">FLOATOBJ_SetLong</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_sub">FLOATOBJ_Sub</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_subfloat">FLOATOBJ_SubFloat</a>



<a href="/windows/desktop/api/winddi/nf-winddi-floatobj_sublong">FLOATOBJ_SubLong</a>



<a href="/windows/desktop/api/winddi/ns-winddi-floatobj_xform">FLOATOBJ_XFORM</a>



<a href="/windows/desktop/api/winddi/nf-winddi-xformobj_igetfloatobjxform">XFORMOBJ_iGetFloatObjXform</a>