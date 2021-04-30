---
UID: NF:winddi.FLOATOBJ_Div
title: FLOATOBJ_Div function (winddi.h)
description: The FLOATOBJ_Div function divides the two FLOATOBJs, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_Div","FLOATOBJ_Div function [Display Devices]","display.floatobj_div","gdifncs_0ffe4b55-d291-47b0-bbd4-351e01ffe228.xml","winddi/FLOATOBJ_Div"]
old-location: display\floatobj_div.htm
tech.root: display
ms.assetid: 110473d8-712a-4670-96e0-daf57dd5efd2
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_Div, FLOATOBJ_Div function [Display Devices], display.floatobj_div, gdifncs_0ffe4b55-d291-47b0-bbd4-351e01ffe228.xml, winddi/FLOATOBJ_Div
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
 - FLOATOBJ_Div
 - winddi/FLOATOBJ_Div
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
 - FLOATOBJ_Div
---

# FLOATOBJ_Div function


## -description

The <b>FLOATOBJ_Div</b> function divides the two <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>s, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the first FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the quotient of *<i>pf</i> divided by *<i>pf1</i>.

### -param unnamedParam2 [in]

Pointer to the second FLOATOBJ operand.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>