---
UID: NF:winddi.FLOATOBJ_AddFloat
title: FLOATOBJ_AddFloat function (winddi.h)
description: The FLOATOBJ_AddFloat function adds the value of type FLOATL to the FLOATOBJ, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_AddFloat","FLOATOBJ_AddFloat function [Display Devices]","display.floatobj_addfloat","gdifncs_2e5305b6-571f-4ae2-bfd7-2305c006b6da.xml","winddi/FLOATOBJ_AddFloat"]
old-location: display\floatobj_addfloat.htm
tech.root: display
ms.assetid: 47af86ec-a7b2-49c1-aeda-1a273f17c4ae
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_AddFloat, FLOATOBJ_AddFloat function [Display Devices], display.floatobj_addfloat, gdifncs_2e5305b6-571f-4ae2-bfd7-2305c006b6da.xml, winddi/FLOATOBJ_AddFloat
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
 - FLOATOBJ_AddFloat
 - winddi/FLOATOBJ_AddFloat
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
 - FLOATOBJ_AddFloat
---

# FLOATOBJ_AddFloat function


## -description

The <b>FLOATOBJ_AddFloat</b> function adds the value of type FLOATL to the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the sum of *<i>pf</i> and *<i>f</i>.

### -param unnamedParam2 [in]

Specifies the FLOATL operand. This value is converted to a FLOATOBJ for the summation.

## -remarks

The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>