---
UID: NF:winddi.FLOATOBJ_SubLong
title: FLOATOBJ_SubLong function (winddi.h)
description: The FLOATOBJ_SubLong function subtracts the value of type LONG from the FLOATOBJ, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_SubLong","FLOATOBJ_SubLong function [Display Devices]","display.floatobj_sublong","gdifncs_8b50c7a1-6ed7-4368-8465-5b1b1e7f4c48.xml","winddi/FLOATOBJ_SubLong"]
old-location: display\floatobj_sublong.htm
tech.root: display
ms.assetid: 2a3e8a17-3718-4212-adfe-f109e286bec6
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_SubLong, FLOATOBJ_SubLong function [Display Devices], display.floatobj_sublong, gdifncs_8b50c7a1-6ed7-4368-8465-5b1b1e7f4c48.xml, winddi/FLOATOBJ_SubLong
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
 - FLOATOBJ_SubLong
 - winddi/FLOATOBJ_SubLong
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
 - FLOATOBJ_SubLong
---

# FLOATOBJ_SubLong function


## -description

The <b>FLOATOBJ_SubLong</b> function subtracts the value of type LONG from the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i> - <i>l</i>).

### -param unnamedParam2 [in]

Specifies the LONG operand. This value is converted to a FLOATOBJ for the subtraction.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>