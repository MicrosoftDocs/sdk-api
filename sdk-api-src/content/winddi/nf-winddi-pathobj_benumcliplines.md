---
UID: NF:winddi.PATHOBJ_bEnumClipLines
title: PATHOBJ_bEnumClipLines function (winddi.h)
description: The PATHOBJ_bEnumClipLines function enumerates clipped line segments from a given path.
helpviewer_keywords: ["PATHOBJ_bEnumClipLines","PATHOBJ_bEnumClipLines function [Display Devices]","display.pathobj_benumcliplines","gdifncs_39da05f4-124b-4d0f-b33b-777220462aa7.xml","winddi/PATHOBJ_bEnumClipLines"]
old-location: display\pathobj_benumcliplines.htm
tech.root: display
ms.assetid: edc64b1e-dd3f-4b6a-858c-91c49a819b0a
ms.date: 12/05/2018
ms.keywords: PATHOBJ_bEnumClipLines, PATHOBJ_bEnumClipLines function [Display Devices], display.pathobj_benumcliplines, gdifncs_39da05f4-124b-4d0f-b33b-777220462aa7.xml, winddi/PATHOBJ_bEnumClipLines
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
 - PATHOBJ_bEnumClipLines
 - winddi/PATHOBJ_bEnumClipLines
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
 - PATHOBJ_bEnumClipLines
---

# PATHOBJ_bEnumClipLines function


## -description

The <b>PATHOBJ_bEnumClipLines</b> function enumerates clipped line segments from a given path.

## -parameters

### -param ppo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure containing the clipped line segments that are to be enumerated.

### -param cb

Specifies the size of the output buffer, in bytes. GDI does not write beyond this point in the buffer. The value of this parameter must be large enough to hold a <a href="/windows/desktop/api/winddi/ns-winddi-clipline">CLIPLINE</a> structure with at least one <a href="/windows/desktop/api/winddi/ns-winddi-run">RUN</a> structure. The driver should allocate space for several RUN structures.

### -param pcl

Pointer to the buffer that receives a CLIPLINE structure. The structure contains the original unclipped control points for a line segment. (The correct pixels for the line cannot be computed without the original points.) RUN structures, which describe sets of pixels along the line that are not clipped away, are written to this buffer.

If a clip region is complex, a single line segment can be broken into many RUN structures. A segment is returned as many times as necessary to list all of its RUN structures.

The CLIPLINE structure contains the starting and ending points of the original unclipped line and the line segments, or RUN structures, of that line that are to appear on the display.

## -returns

The return value is <b>TRUE</b> if more line segments are to be enumerated, indicating that this service should be called again. Otherwise, it is <b>FALSE</b>, indicating that the returned segment is the last segment in the path.

## -remarks

The enumeration must be started with <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_venumstartcliplines">PATHOBJ_vEnumStartClipLines</a> before the driver makes this call.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipline">CLIPLINE</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_venumstartcliplines">PATHOBJ_vEnumStartClipLines</a>



<a href="/windows/desktop/api/winddi/ns-winddi-run">RUN</a>