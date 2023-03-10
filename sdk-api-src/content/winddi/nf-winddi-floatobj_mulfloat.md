---
UID: NF:winddi.FLOATOBJ_MulFloat
title: FLOATOBJ_MulFloat function (winddi.h)
description: The FLOATOBJ_MulFloat function multiplies the FLOATOBJ by the value of type FLOATL, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_MulFloat","FLOATOBJ_MulFloat function [Display Devices]","display.floatobj_mulfloat","gdifncs_39da7310-f7d3-4ceb-8bd5-c2a0eaab0068.xml","winddi/FLOATOBJ_MulFloat"]
old-location: display\floatobj_mulfloat.htm
tech.root: display
ms.assetid: 7b4189f7-b80b-4543-b713-b0b2d06ef81e
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_MulFloat, FLOATOBJ_MulFloat function [Display Devices], display.floatobj_mulfloat, gdifncs_39da7310-f7d3-4ceb-8bd5-c2a0eaab0068.xml, winddi/FLOATOBJ_MulFloat
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
 - FLOATOBJ_MulFloat
 - winddi/FLOATOBJ_MulFloat
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
 - FLOATOBJ_MulFloat
---

# FLOATOBJ_MulFloat function


## -description

The <b>FLOATOBJ_MulFloat</b> function multiplies the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a> by the value of type FLOATL, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i>  *  <i>f</i>).

### -param unnamedParam2 [in]

Specifies the FLOATL operand. This value is converted to a FLOATOBJ for the multiplication.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>