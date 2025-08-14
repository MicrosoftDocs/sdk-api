---
UID: NF:winddi.BRUSHOBJ_hGetColorTransform
title: BRUSHOBJ_hGetColorTransform function (winddi.h)
description: The BRUSHOBJ_hGetColorTransform function retrieves the color transform for the specified brush.
helpviewer_keywords: ["BRUSHOBJ_hGetColorTransform","BRUSHOBJ_hGetColorTransform function [Display Devices]","display.brushobj_hgetcolortransform","gdifncs_eeb575c7-44b8-4af6-ab2d-6bb1afc3af32.xml","winddi/BRUSHOBJ_hGetColorTransform"]
old-location: display\brushobj_hgetcolortransform.htm
tech.root: display
ms.assetid: a62544e5-f4b6-4544-8ec1-5a03f8bd3306
ms.date: 12/05/2018
ms.keywords: BRUSHOBJ_hGetColorTransform, BRUSHOBJ_hGetColorTransform function [Display Devices], display.brushobj_hgetcolortransform, gdifncs_eeb575c7-44b8-4af6-ab2d-6bb1afc3af32.xml, winddi/BRUSHOBJ_hGetColorTransform
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
 - BRUSHOBJ_hGetColorTransform
 - winddi/BRUSHOBJ_hGetColorTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - BRUSHOBJ_hGetColorTransform
---

# BRUSHOBJ_hGetColorTransform function


## -description

The <b>BRUSHOBJ_hGetColorTransform</b> function retrieves the color transform for the specified brush.

## -parameters

### -param pbo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure whose color transform is being queried. The color transform was created in a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-drvicmcreatecolortransform">DrvIcmCreateColorTransform</a>.

## -returns

<b>BRUSHOBJ_hGetColorTransform</b> returns a handle to the color transform for the specified BRUSHOBJ structure upon success. Otherwise, it returns <b>NULL</b>.

## -remarks

<b>BRUSHOBJ_hGetColorTransform</b> returns <b>NULL</b> when ICM is disabled.

The color transform for a translation object is obtained by calling <a href="/windows/desktop/api/winddi/nf-winddi-xlateobj_hgetcolortransform">XLATEOBJ_hGetColorTransform</a>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvicmcreatecolortransform">DrvIcmCreateColorTransform</a>



<a href="/windows/desktop/api/winddi/nf-winddi-xlateobj_hgetcolortransform">XLATEOBJ_hGetColorTransform</a>