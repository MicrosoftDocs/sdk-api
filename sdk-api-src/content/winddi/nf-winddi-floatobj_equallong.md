---
UID: NF:winddi.FLOATOBJ_EqualLong
title: FLOATOBJ_EqualLong function (winddi.h)
description: The FLOATOBJ_EqualLong function determines whether the FLOATOBJ and the value of type LONG are equal.
helpviewer_keywords: ["FLOATOBJ_EqualLong","FLOATOBJ_EqualLong function [Display Devices]","display.floatobj_equallong","gdifncs_8c714f1b-6b6b-465c-a481-74e3f475338c.xml","winddi/FLOATOBJ_EqualLong"]
old-location: display\floatobj_equallong.htm
tech.root: display
ms.assetid: ab81a183-6517-4353-accb-425f02004577
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_EqualLong, FLOATOBJ_EqualLong function [Display Devices], display.floatobj_equallong, gdifncs_8c714f1b-6b6b-465c-a481-74e3f475338c.xml, winddi/FLOATOBJ_EqualLong
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
 - FLOATOBJ_EqualLong
 - winddi/FLOATOBJ_EqualLong
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
 - FLOATOBJ_EqualLong
---

# FLOATOBJ_EqualLong function


## -description

The <b>FLOATOBJ_EqualLong</b> function determines whether the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a> and the value of type LONG are equal.

## -parameters

### -param unnamedParam1 [in]

Pointer to the FLOATOBJ.

### -param unnamedParam2 [in]

Specifies the LONG value. This value is converted to a FLOATOBJ for the comparison.

## -returns

<b>FLOATOBJ_EqualLong </b> returns <b>TRUE</b> if *<i>pf</i> and the FLOATOBJ-equivalent value of <i>l</i> are equal; otherwise it returns <b>FALSE</b>.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>