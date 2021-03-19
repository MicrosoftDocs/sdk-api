---
UID: NF:winddi.FLOATOBJ_Add
title: FLOATOBJ_Add function (winddi.h)
description: The FLOATOBJ_Add function adds the two FLOATOBJs, and returns with the result in the first parameter.
helpviewer_keywords: ["FLOATOBJ_Add","FLOATOBJ_Add function [Display Devices]","display.floatobj_add","gdifncs_484fa853-6c4e-4bc1-95a3-7f7b40828fcc.xml","winddi/FLOATOBJ_Add"]
old-location: display\floatobj_add.htm
tech.root: display
ms.assetid: 6502d863-ab3e-46d2-8da4-c2f1b01fe344
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_Add, FLOATOBJ_Add function [Display Devices], display.floatobj_add, gdifncs_484fa853-6c4e-4bc1-95a3-7f7b40828fcc.xml, winddi/FLOATOBJ_Add
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
 - FLOATOBJ_Add
 - winddi/FLOATOBJ_Add
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
 - FLOATOBJ_Add
---

# FLOATOBJ_Add function


## -description

The <b>FLOATOBJ_Add</b> function adds the two FLOATOBJs, and returns with the result in the first parameter.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the first FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the sum of *<i>pf</i> and *<i>pf1</i>.

### -param unnamedParam2 [in]

Pointer to the second FLOATOBJ operand.

## -remarks

The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>