---
UID: NF:winddi.FLOATOBJ_DivFloat
title: FLOATOBJ_DivFloat function (winddi.h)
description: The FLOATOBJ_DivFloat function divides the FLOATOBJ by the value of type FLOATL, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_DivFloat","FLOATOBJ_DivFloat function [Display Devices]","display.floatobj_divfloat","gdifncs_b815b21c-c9fb-4334-857f-e6e66053014a.xml","winddi/FLOATOBJ_DivFloat"]
old-location: display\floatobj_divfloat.htm
tech.root: display
ms.assetid: 47ebf68c-6dfa-43d3-8bc9-1f0b8f030974
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_DivFloat, FLOATOBJ_DivFloat function [Display Devices], display.floatobj_divfloat, gdifncs_b815b21c-c9fb-4334-857f-e6e66053014a.xml, winddi/FLOATOBJ_DivFloat
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
 - FLOATOBJ_DivFloat
 - winddi/FLOATOBJ_DivFloat
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
 - FLOATOBJ_DivFloat
---

# FLOATOBJ_DivFloat function


## -description

The <b>FLOATOBJ_DivFloat</b> function divides the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a> by the value of type FLOATL, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the quotient of *<i>pf</i> divided by <i>f</i>.

### -param unnamedParam2 [in]

Specifies the FLOATL operand. This value is converted to a FLOATOBJ for the division.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>