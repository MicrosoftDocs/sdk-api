---
UID: NF:winddi.FLOATOBJ_Equal
title: FLOATOBJ_Equal function (winddi.h)
description: The FLOATOBJ_Equal function determines whether the two FLOATOBJs are equal.
helpviewer_keywords: ["FLOATOBJ_Equal","FLOATOBJ_Equal function [Display Devices]","display.floatobj_equal","gdifncs_20ba1db5-2709-4765-a637-94000c803ecb.xml","winddi/FLOATOBJ_Equal"]
old-location: display\floatobj_equal.htm
tech.root: display
ms.assetid: 1fc9afcb-7b65-415c-ae6c-8885ef47abe9
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_Equal, FLOATOBJ_Equal function [Display Devices], display.floatobj_equal, gdifncs_20ba1db5-2709-4765-a637-94000c803ecb.xml, winddi/FLOATOBJ_Equal
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
 - FLOATOBJ_Equal
 - winddi/FLOATOBJ_Equal
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
 - FLOATOBJ_Equal
---

# FLOATOBJ_Equal function


## -description

The <b>FLOATOBJ_Equal</b> function determines whether the two <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>s are equal.

## -parameters

### -param unnamedParam1 [in]

Pointer to the first FLOATOBJ operand.

### -param unnamedParam2 [in]

Pointer to the second FLOATOBJ operand.

## -returns

<b>FLOATOBJ_Equal </b> returns <b>TRUE</b> if *<i>pf</i> and *<i>pf1</i> are equal; otherwise it returns <b>FALSE</b>.

## -remarks

The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>