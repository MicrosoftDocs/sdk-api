---
UID: NF:winddi.FLOATOBJ_SetFloat
title: FLOATOBJ_SetFloat function (winddi.h)
description: The FLOATOBJ_SetFloat function assigns the value of type FLOATL to the FLOATOBJ.
helpviewer_keywords: ["FLOATOBJ_SetFloat","FLOATOBJ_SetFloat function [Display Devices]","display.floatobj_setfloat","gdifncs_3bf0c118-feea-48f1-8e20-d3b43408a860.xml","winddi/FLOATOBJ_SetFloat"]
old-location: display\floatobj_setfloat.htm
tech.root: display
ms.assetid: ba2c33fa-9489-482d-b27e-79537425cc4b
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_SetFloat, FLOATOBJ_SetFloat function [Display Devices], display.floatobj_setfloat, gdifncs_3bf0c118-feea-48f1-8e20-d3b43408a860.xml, winddi/FLOATOBJ_SetFloat
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FLOATOBJ_SetFloat
 - winddi/FLOATOBJ_SetFloat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FLOATOBJ_SetFloat
---

# FLOATOBJ_SetFloat function


## -description

The <b>FLOATOBJ_SetFloat</b> function assigns the value of type FLOATL to the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>.

## -parameters

### -param unnamedParam1 [out]

Pointer to the FLOATOBJ that will receive the value of <i>f</i>.

### -param unnamedParam2 [in]

Specifies the FLOATL value. This value is converted to a FLOATOBJ for the assignment.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>