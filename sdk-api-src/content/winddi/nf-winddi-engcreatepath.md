---
UID: NF:winddi.EngCreatePath
title: EngCreatePath function (winddi.h)
description: The EngCreatePath function allocates a path for the driver's temporary use.
helpviewer_keywords: ["EngCreatePath","EngCreatePath function [Display Devices]","display.engcreatepath","gdifncs_73e7c8ea-ed9f-4479-bd8a-86a5d07e5d33.xml","winddi/EngCreatePath"]
old-location: display\engcreatepath.htm
tech.root: display
ms.assetid: b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a
ms.date: 12/05/2018
ms.keywords: EngCreatePath, EngCreatePath function [Display Devices], display.engcreatepath, gdifncs_73e7c8ea-ed9f-4479-bd8a-86a5d07e5d33.xml, winddi/EngCreatePath
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
 - EngCreatePath
 - winddi/EngCreatePath
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
 - EngCreatePath
---

# EngCreatePath function


## -description

The <b>EngCreatePath</b> function allocates a path for the driver's temporary use.



## -returns

The return value is a pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure if the function is successful. Otherwise, it is null, and an error code is logged.

## -remarks

The driver should delete the path, allocated by <b>EngCreatePath</b>, before returning to GDI from its current drawing call.

Functions that create and modify paths are provided to assist devices in clipping paths. A driver can create a path, fill it with lines and pass the path to <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a> for clipping against the complex region.

A PATHOBJ structure is a locked object, and thus should not be locked for a long time by the driver.

If the driver uses <b>EngCreatePath</b> to create a PATHOBJ structure, it should be deleted by using <a href="/windows/desktop/api/winddi/nf-winddi-engdeletepath">EngDeletePath</a> as soon as the driver finishes with it.

The returned PATHOBJ structure is used in calls to <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bmoveto">PATHOBJ_bMoveTo</a>, <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bpolylineto">PATHOBJ_bPolyLineTo</a>, <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_venumstartcliplines">PATHOBJ_vEnumStartClipLines</a>, and <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a>

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a>
