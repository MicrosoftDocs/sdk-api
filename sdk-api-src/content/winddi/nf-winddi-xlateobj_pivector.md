---
UID: NF:winddi.XLATEOBJ_piVector
title: XLATEOBJ_piVector function (winddi.h)
description: The XLATEOBJ_piVector function retrieves a translation vector that the driver can use to translate source indices to destination indices.
helpviewer_keywords: ["XLATEOBJ_piVector","XLATEOBJ_piVector function [Display Devices]","display.xlateobj_pivector","gdifncs_875168b9-8752-46cb-9198-53af5769db5b.xml","winddi/XLATEOBJ_piVector"]
old-location: display\xlateobj_pivector.htm
tech.root: display
ms.assetid: 7dcfd280-26af-47ff-a5a6-50325e6471bc
ms.date: 12/05/2018
ms.keywords: XLATEOBJ_piVector, XLATEOBJ_piVector function [Display Devices], display.xlateobj_pivector, gdifncs_875168b9-8752-46cb-9198-53af5769db5b.xml, winddi/XLATEOBJ_piVector
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
 - XLATEOBJ_piVector
 - winddi/XLATEOBJ_piVector
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - XLATEOBJ_piVector
---

# XLATEOBJ_piVector function


## -description

The <b>XLATEOBJ_piVector</b> function retrieves a translation vector that the driver can use to translate source indices to destination indices.

## -parameters

### -param pxlo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines the indexed source object.

## -returns

The return value is a pointer to a vector of translation entries if the function is successful. Otherwise, it is null, and an error code is logged.

## -remarks

This function can be used only if the source palette is an indexed palette.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>