---
UID: NF:winddi.PATHOBJ_bMoveTo
title: PATHOBJ_bMoveTo function (winddi.h)
description: The PATHOBJ_bMoveTo function sets the current position in a given path.
helpviewer_keywords: ["PATHOBJ_bMoveTo","PATHOBJ_bMoveTo function [Display Devices]","display.pathobj_bmoveto","gdifncs_a6917397-5fcb-41fd-8f5a-f6af95ee7bb2.xml","winddi/PATHOBJ_bMoveTo"]
old-location: display\pathobj_bmoveto.htm
tech.root: display
ms.assetid: b734ce8f-7e7e-4c13-a614-cb6b0dc19ead
ms.date: 12/05/2018
ms.keywords: PATHOBJ_bMoveTo, PATHOBJ_bMoveTo function [Display Devices], display.pathobj_bmoveto, gdifncs_a6917397-5fcb-41fd-8f5a-f6af95ee7bb2.xml, winddi/PATHOBJ_bMoveTo
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
 - PATHOBJ_bMoveTo
 - winddi/PATHOBJ_bMoveTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - PATHOBJ_bMoveTo
---

# PATHOBJ_bMoveTo function


## -description

The <b>PATHOBJ_bMoveTo</b> function sets the current position in a given path.

## -parameters

### -param ppo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure created by the driver.

### -param ptfx

Pointer to a POINTFIX structure that specifies the new position. For a description of this data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

This function should only be called with PATHOBJ structures created by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>