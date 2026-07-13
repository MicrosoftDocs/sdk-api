---
UID: NF:winddi.CLIPOBJ_ppoGetPath
title: CLIPOBJ_ppoGetPath function (winddi.h)
description: The CLIPOBJ_ppoGetPath function creates a PATHOBJ structure that contains the outline of the specified clip region.
helpviewer_keywords: ["CLIPOBJ_ppoGetPath","CLIPOBJ_ppoGetPath function [Display Devices]","display.clipobj_ppogetpath","gdifncs_576284af-4aef-45be-b10a-2504c8e3451f.xml","winddi/CLIPOBJ_ppoGetPath"]
old-location: display\clipobj_ppogetpath.htm
tech.root: display
ms.assetid: c87d1580-ab24-49a7-b497-87d781be6e5f
ms.date: 12/05/2018
ms.keywords: CLIPOBJ_ppoGetPath, CLIPOBJ_ppoGetPath function [Display Devices], display.clipobj_ppogetpath, gdifncs_576284af-4aef-45be-b10a-2504c8e3451f.xml, winddi/CLIPOBJ_ppoGetPath
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
 - CLIPOBJ_ppoGetPath
 - winddi/CLIPOBJ_ppoGetPath
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
 - CLIPOBJ_ppoGetPath
---

# CLIPOBJ_ppoGetPath function


## -description

The <b>CLIPOBJ_ppoGetPath</b> function creates a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure that contains the outline of the specified clip region.

## -parameters

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that defines the specified clip region.

## -returns

The return value is a pointer to a PATHOBJ structure if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.

## -remarks

The returned PATHOBJ structure should be deleted using <a href="/windows/desktop/api/winddi/nf-winddi-engdeletepath">EngDeletePath</a> when the driver no longer needs it.

A driver for a device that can download a clipping path might prefer this function for defining complex regions.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletepath">EngDeletePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>