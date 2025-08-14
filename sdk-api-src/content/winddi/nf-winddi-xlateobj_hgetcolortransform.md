---
UID: NF:winddi.XLATEOBJ_hGetColorTransform
title: XLATEOBJ_hGetColorTransform function (winddi.h)
description: The XLATEOBJ_hGetColorTransform function returns the color transform for the specified translation object.
helpviewer_keywords: ["XLATEOBJ_hGetColorTransform","XLATEOBJ_hGetColorTransform function [Display Devices]","display.xlateobj_hgetcolortransform","gdifncs_6df99fb8-f6ad-4fe8-a140-c004700b9d33.xml","winddi/XLATEOBJ_hGetColorTransform"]
old-location: display\xlateobj_hgetcolortransform.htm
tech.root: display
ms.assetid: dd109ae8-c368-4e8a-bf25-405ed96484e3
ms.date: 12/05/2018
ms.keywords: XLATEOBJ_hGetColorTransform, XLATEOBJ_hGetColorTransform function [Display Devices], display.xlateobj_hgetcolortransform, gdifncs_6df99fb8-f6ad-4fe8-a140-c004700b9d33.xml, winddi/XLATEOBJ_hGetColorTransform
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
 - XLATEOBJ_hGetColorTransform
 - winddi/XLATEOBJ_hGetColorTransform
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
 - XLATEOBJ_hGetColorTransform
---

# XLATEOBJ_hGetColorTransform function


## -description

The <b>XLATEOBJ_hGetColorTransform</b> function returns the color transform for the specified translation object.

## -parameters

### -param pxlo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure whose color transform is being queried. The color transform was created in a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-drvicmcreatecolortransform">DrvIcmCreateColorTransform</a>.

## -returns

<b>XLATEOBJ_hGetColorTransform</b> returns a handle to the color transform for the specified XLATEOBJ upon success. Otherwise, it returns <b>NULL</b>.

## -remarks

<b>XLATEOBJ_hGetColorTransform</b> returns <b>NULL</b> when it is called in host ICM context or when ICM is disabled.

The color transform for a brush is obtained by calling <a href="/windows/desktop/api/winddi/nf-winddi-brushobj_hgetcolortransform">BRUSHOBJ_hGetColorTransform</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-brushobj_hgetcolortransform">BRUSHOBJ_hGetColorTransform</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvicmcreatecolortransform">DrvIcmCreateColorTransform</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>