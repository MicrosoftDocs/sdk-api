---
UID: NF:winddi.FLOATOBJ_Mul
title: FLOATOBJ_Mul function (winddi.h)
description: The FLOATOBJ_Mul function multiplies the two FLOATOBJs, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_Mul","FLOATOBJ_Mul function [Display Devices]","display.floatobj_mul","gdifncs_1647a791-7781-4e67-a7b1-06b283c32b0b.xml","winddi/FLOATOBJ_Mul"]
old-location: display\floatobj_mul.htm
tech.root: display
ms.assetid: 95b4c3eb-5e62-4209-9c05-eae9ab48f7ab
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_Mul, FLOATOBJ_Mul function [Display Devices], display.floatobj_mul, gdifncs_1647a791-7781-4e67-a7b1-06b283c32b0b.xml, winddi/FLOATOBJ_Mul
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
 - FLOATOBJ_Mul
 - winddi/FLOATOBJ_Mul
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
 - FLOATOBJ_Mul
---

# FLOATOBJ_Mul function


## -description

The <b>FLOATOBJ_Mul</b> function multiplies the two <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>s, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the first FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value ( *<i>pf</i>  *  *<i>pf1</i>).

### -param unnamedParam2 [in]

Pointer to the second FLOATOBJ operand.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>