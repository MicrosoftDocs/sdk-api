---
UID: NF:winddi.FLOATOBJ_MulLong
title: FLOATOBJ_MulLong function (winddi.h)
description: The FLOATOBJ_MulLong function multiplies the FLOATOBJ by the value of type LONG, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_MulLong","FLOATOBJ_MulLong function [Display Devices]","display.floatobj_mullong","gdifncs_7548db1a-4ed7-4946-95f6-5541e7c4226f.xml","winddi/FLOATOBJ_MulLong"]
old-location: display\floatobj_mullong.htm
tech.root: display
ms.assetid: 945b9280-41fc-44f9-a5df-c0a725cef377
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_MulLong, FLOATOBJ_MulLong function [Display Devices], display.floatobj_mullong, gdifncs_7548db1a-4ed7-4946-95f6-5541e7c4226f.xml, winddi/FLOATOBJ_MulLong
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
 - FLOATOBJ_MulLong
 - winddi/FLOATOBJ_MulLong
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
 - FLOATOBJ_MulLong
---

# FLOATOBJ_MulLong function


## -description

The <b>FLOATOBJ_MulLong</b> function multiplies the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a> by the value of type LONG, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value ( *<i>pf</i>  *  <i>l</i>).

### -param unnamedParam2 [in]

Specifies the LONG operand. This value is converted to a FLOATOBJ for the multiplication.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>