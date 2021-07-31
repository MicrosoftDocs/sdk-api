---
UID: NF:winddi.FLOATOBJ_LessThanLong
title: FLOATOBJ_LessThanLong function (winddi.h)
description: The FLOATOBJ_LessThanLong function determines whether the FLOATOBJ is less than the value of type LONG.
helpviewer_keywords: ["FLOATOBJ_LessThanLong","FLOATOBJ_LessThanLong function [Display Devices]","display.floatobj_lessthanlong","gdifncs_ab38a262-384e-441b-8e87-665a29124cba.xml","winddi/FLOATOBJ_LessThanLong"]
old-location: display\floatobj_lessthanlong.htm
tech.root: display
ms.assetid: 10665f5d-68ae-4f72-9fa2-c79cf86ded3d
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_LessThanLong, FLOATOBJ_LessThanLong function [Display Devices], display.floatobj_lessthanlong, gdifncs_ab38a262-384e-441b-8e87-665a29124cba.xml, winddi/FLOATOBJ_LessThanLong
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
 - FLOATOBJ_LessThanLong
 - winddi/FLOATOBJ_LessThanLong
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
 - FLOATOBJ_LessThanLong
---

# FLOATOBJ_LessThanLong function


## -description

The <b>FLOATOBJ_LessThanLong</b> function determines whether the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a> is less than the value of type LONG.

## -parameters

### -param unnamedParam1 [in]

Pointer to the FLOATOBJ.

### -param unnamedParam2 [in]

Specifies the LONG value. This value is converted to a FLOATOBJ for the comparison.

## -returns

<b>FLOATOBJ_LessThanLong</b> returns <b>TRUE</b> if *<i>pf</i> is less than the FLOATOBJ-equivalent of <i>l</i>; otherwise it returns <b>FALSE</b>.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>
