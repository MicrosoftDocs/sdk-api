---
UID: NF:winddi.FLOATOBJ_SubFloat
title: FLOATOBJ_SubFloat function (winddi.h)
description: The FLOATOBJ_SubFloat function subtracts the value of type FLOATL from the FLOATOBJ, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_SubFloat","FLOATOBJ_SubFloat function [Display Devices]","display.floatobj_subfloat","gdifncs_9f655d6e-8ef0-45e5-9d0e-963a30460920.xml","winddi/FLOATOBJ_SubFloat"]
old-location: display\floatobj_subfloat.htm
tech.root: display
ms.assetid: 0fa69283-3236-43bc-9c16-6bd220ad4e0c
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_SubFloat, FLOATOBJ_SubFloat function [Display Devices], display.floatobj_subfloat, gdifncs_9f655d6e-8ef0-45e5-9d0e-963a30460920.xml, winddi/FLOATOBJ_SubFloat
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
 - FLOATOBJ_SubFloat
 - winddi/FLOATOBJ_SubFloat
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
 - FLOATOBJ_SubFloat
---

# FLOATOBJ_SubFloat function


## -description

The <b>FLOATOBJ_SubFloat</b> function subtracts the value of type FLOATL from the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i> - <i>f</i>).

### -param unnamedParam2 [in]

Specifies the FLOATL operand. This value is converted to a FLOATOBJ for the subtraction.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>