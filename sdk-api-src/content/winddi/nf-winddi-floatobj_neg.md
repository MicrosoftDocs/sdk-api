---
UID: NF:winddi.FLOATOBJ_Neg
title: FLOATOBJ_Neg function (winddi.h)
description: The FLOATOBJ_Neg function negates the FLOATOBJ.
helpviewer_keywords: ["FLOATOBJ_Neg","FLOATOBJ_Neg function [Display Devices]","display.floatobj_neg","gdifncs_7fe9b86a-abdd-44d6-b815-1ac5f37203db.xml","winddi/FLOATOBJ_Neg"]
old-location: display\floatobj_neg.htm
tech.root: display
ms.assetid: 08a4c47f-8bf5-4849-8ce9-e5999c02f263
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_Neg, FLOATOBJ_Neg function [Display Devices], display.floatobj_neg, gdifncs_7fe9b86a-abdd-44d6-b815-1ac5f37203db.xml, winddi/FLOATOBJ_Neg
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
 - FLOATOBJ_Neg
 - winddi/FLOATOBJ_Neg
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
 - FLOATOBJ_Neg
---

# FLOATOBJ_Neg function


## -description

The <b>FLOATOBJ_Neg</b> function negates the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to the FLOATOBJ to be negated. When the function returns, *<i>pf</i> will contain the negated value.

## -remarks

The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>