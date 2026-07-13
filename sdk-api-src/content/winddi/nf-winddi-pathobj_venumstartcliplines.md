---
UID: NF:winddi.PATHOBJ_vEnumStartClipLines
title: PATHOBJ_vEnumStartClipLines function (winddi.h)
description: The PATHOBJ_vEnumStartClipLines function allows the driver to request lines to be clipped against a specified clip region.
helpviewer_keywords: ["PATHOBJ_vEnumStartClipLines","PATHOBJ_vEnumStartClipLines function [Display Devices]","display.pathobj_venumstartcliplines","gdifncs_f5446bec-830c-4946-b899-1d9a957b44ef.xml","winddi/PATHOBJ_vEnumStartClipLines"]
old-location: display\pathobj_venumstartcliplines.htm
tech.root: display
ms.assetid: 3db437aa-40d1-4703-ab1e-b3e154923d2d
ms.date: 12/05/2018
ms.keywords: PATHOBJ_vEnumStartClipLines, PATHOBJ_vEnumStartClipLines function [Display Devices], display.pathobj_venumstartcliplines, gdifncs_f5446bec-830c-4946-b899-1d9a957b44ef.xml, winddi/PATHOBJ_vEnumStartClipLines
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
 - PATHOBJ_vEnumStartClipLines
 - winddi/PATHOBJ_vEnumStartClipLines
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
 - PATHOBJ_vEnumStartClipLines
---

# PATHOBJ_vEnumStartClipLines function


## -description

The <b>PATHOBJ_vEnumStartClipLines</b> function allows the driver to request lines to be clipped against a specified clip region.

## -parameters

### -param ppo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure that describes the specified clipping object.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that describes the clip region.

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that GDI queries to retrieve information about styling steps.

### -param pla

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a> structure that GDI queries to retrieve line width and styling information.

## -returns

None

## -remarks

This function is useful when the clip region is more complex than a simple rectangle.

<b>PATHOBJ_vEnumStartClipLines</b> performs calculations for cosmetic wide lines. If the LINEATTRS structure needs a cosmetic wide line, the enumeration walks the given path as many times as needed to complete the widened figure.

This function should not be called for geometric wide lines or paths that contain Bezier curves.

Once begun, this enumeration process should not be restarted.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>