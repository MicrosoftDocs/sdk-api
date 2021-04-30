---
UID: NF:winddi.FLOATOBJ_SetLong
title: FLOATOBJ_SetLong function (winddi.h)
description: The FLOATOBJ_SetLong function assigns the value of type LONG to the FLOATOBJ.
helpviewer_keywords: ["FLOATOBJ_SetLong","FLOATOBJ_SetLong function [Display Devices]","display.floatobj_setlong","gdifncs_b0a076a3-766b-42fb-a04d-5da69177656b.xml","winddi/FLOATOBJ_SetLong"]
old-location: display\floatobj_setlong.htm
tech.root: display
ms.assetid: 4fa1b8a6-8172-4047-9ee2-fe00f0924487
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_SetLong, FLOATOBJ_SetLong function [Display Devices], display.floatobj_setlong, gdifncs_b0a076a3-766b-42fb-a04d-5da69177656b.xml, winddi/FLOATOBJ_SetLong
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
 - FLOATOBJ_SetLong
 - winddi/FLOATOBJ_SetLong
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
 - FLOATOBJ_SetLong
---

# FLOATOBJ_SetLong function


## -description

The <b>FLOATOBJ_SetLong</b> function assigns the value of type LONG to the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>.

## -parameters

### -param unnamedParam1 [out]

Pointer to the FLOATOBJ that will receive the value of <i>l</i>.

### -param unnamedParam2 [in]

Specifies the LONG value. This value is converted to a FLOATOBJ for the assignment.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>