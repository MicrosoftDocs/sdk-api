---
UID: NF:winddi.FLOATOBJ_GreaterThan
title: FLOATOBJ_GreaterThan function (winddi.h)
description: The FLOATOBJ_GreaterThan function determines whether the first FLOATOBJ is greater than the second FLOATOBJ.
helpviewer_keywords: ["FLOATOBJ_GreaterThan","FLOATOBJ_GreaterThan function [Display Devices]","display.floatobj_greaterthan","gdifncs_ac52408a-8df9-4fe2-bf33-35bdfb9fa5d8.xml","winddi/FLOATOBJ_GreaterThan"]
old-location: display\floatobj_greaterthan.htm
tech.root: display
ms.assetid: 45e743e4-a72d-413a-9ee3-79eab517c87e
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_GreaterThan, FLOATOBJ_GreaterThan function [Display Devices], display.floatobj_greaterthan, gdifncs_ac52408a-8df9-4fe2-bf33-35bdfb9fa5d8.xml, winddi/FLOATOBJ_GreaterThan
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
 - FLOATOBJ_GreaterThan
 - winddi/FLOATOBJ_GreaterThan
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
 - FLOATOBJ_GreaterThan
---

# FLOATOBJ_GreaterThan function


## -description

The <b>FLOATOBJ_GreaterThan</b> function determines whether the first <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a> is greater than the second FLOATOBJ.

## -parameters

### -param unnamedParam1 [in]

Pointer to the first FLOATOBJ.

### -param unnamedParam2 [in]

Pointer to the second FLOATOBJ.

## -returns

<b>FLOATOBJ_GreaterThan </b> returns <b>TRUE</b> if *<i>pf</i> is greater than *<i>pf1</i>; otherwise it returns <b>FALSE</b>.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>