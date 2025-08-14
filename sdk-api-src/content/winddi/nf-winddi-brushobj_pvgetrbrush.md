---
UID: NF:winddi.BRUSHOBJ_pvGetRbrush
title: BRUSHOBJ_pvGetRbrush function (winddi.h)
description: The BRUSHOBJ_pvGetRbrush function retrieves a pointer to the driver's realization of a specified brush.
helpviewer_keywords: ["BRUSHOBJ_pvGetRbrush","BRUSHOBJ_pvGetRbrush function [Display Devices]","display.brushobj_pvgetrbrush","gdifncs_a19def34-749c-4e98-b03e-1b35f4e1f761.xml","winddi/BRUSHOBJ_pvGetRbrush"]
old-location: display\brushobj_pvgetrbrush.htm
tech.root: display
ms.assetid: 3f3e5acb-f984-4571-9555-f6b383ddb6a7
ms.date: 12/05/2018
ms.keywords: BRUSHOBJ_pvGetRbrush, BRUSHOBJ_pvGetRbrush function [Display Devices], display.brushobj_pvgetrbrush, gdifncs_a19def34-749c-4e98-b03e-1b35f4e1f761.xml, winddi/BRUSHOBJ_pvGetRbrush
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
 - BRUSHOBJ_pvGetRbrush
 - winddi/BRUSHOBJ_pvGetRbrush
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
 - BRUSHOBJ_pvGetRbrush
---

# BRUSHOBJ_pvGetRbrush function


## -description

The <b>BRUSHOBJ_pvGetRbrush</b> function retrieves a pointer to the driver's realization of a specified brush.

## -parameters

### -param pbo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure whose realization is requested.

## -returns

The return value is a pointer to the realized brush if the function is successful. If the brush cannot be realized, the return value is null and an error code is logged.

## -remarks

<b>BRUSHOBJ_pvGetRbrush</b> is called when the brush is a pattern brush that has not yet been realized; that is, it is called when the <b>iSolidColor</b> member of the BRUSHOBJ structure is 0xFFFFFFFF and the <b>pvRbrush</b> member is null.

If the brush has not been realized when <b>BRUSHOBJ_pvGetRbrush</b> is called, GDI calls the driver-supplied <a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a> function to obtain the driver's realization of the brush. As an acceleration, GDI caches this realization in the <b>pvRbrush</b> member of the BRUSHOBJ structure. Then, when an application reuses this brush for another drawing operation, the driver doesn't have to call <b>BRUSHOBJ_pvGetRbrush</b> again.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvallocrbrush">BRUSHOBJ_pvAllocRbrush</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a>