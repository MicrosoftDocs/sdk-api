---
UID: NF:winddi.BRUSHOBJ_pvAllocRbrush
title: BRUSHOBJ_pvAllocRbrush function (winddi.h)
description: The BRUSHOBJ_pvAllocRbrush function allocates memory for the driver's realization of a specified brush.
helpviewer_keywords: ["BRUSHOBJ_pvAllocRbrush","BRUSHOBJ_pvAllocRbrush function [Display Devices]","display.brushobj_pvallocrbrush","gdifncs_1858340b-edd3-4fbb-b214-6863301a93fa.xml","winddi/BRUSHOBJ_pvAllocRbrush"]
old-location: display\brushobj_pvallocrbrush.htm
tech.root: display
ms.assetid: 10900536-6c48-4a96-92d2-025660ccff7e
ms.date: 12/05/2018
ms.keywords: BRUSHOBJ_pvAllocRbrush, BRUSHOBJ_pvAllocRbrush function [Display Devices], display.brushobj_pvallocrbrush, gdifncs_1858340b-edd3-4fbb-b214-6863301a93fa.xml, winddi/BRUSHOBJ_pvAllocRbrush
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
 - BRUSHOBJ_pvAllocRbrush
 - winddi/BRUSHOBJ_pvAllocRbrush
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
 - BRUSHOBJ_pvAllocRbrush
---

# BRUSHOBJ_pvAllocRbrush function


## -description

The <b>BRUSHOBJ_pvAllocRbrush</b> function allocates memory for the driver's realization of a specified brush.

## -parameters

### -param pbo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure for which the realization is to be allocated.

### -param cj

Specifies the size, in bytes, required for the realization.

## -returns

The return value is a pointer to the allocated memory if the function is successful. Otherwise, it is null, and an error code is logged.

## -remarks

<b>BRUSHOBJ_pvAllocRbrush</b> allocates memory for the brush realization. GDI manages the memory and discards it when the brush is no longer needed.

This function should be called only by an implementation of a brush realization following a call to <a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a>