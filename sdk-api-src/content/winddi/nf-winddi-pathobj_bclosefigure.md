---
UID: NF:winddi.PATHOBJ_bCloseFigure
title: PATHOBJ_bCloseFigure function (winddi.h)
description: The PATHOBJ_bCloseFigure function closes an open figure in a path by drawing a line from the current position to the first point of the figure.
helpviewer_keywords: ["PATHOBJ_bCloseFigure","PATHOBJ_bCloseFigure function [Display Devices]","display.pathobj_bclosefigure","gdifncs_49059159-bb68-43f7-acd1-2ea665e0db93.xml","winddi/PATHOBJ_bCloseFigure"]
old-location: display\pathobj_bclosefigure.htm
tech.root: display
ms.assetid: e44fb1e3-3d6f-4ff4-83a7-b539d2b570aa
ms.date: 12/05/2018
ms.keywords: PATHOBJ_bCloseFigure, PATHOBJ_bCloseFigure function [Display Devices], display.pathobj_bclosefigure, gdifncs_49059159-bb68-43f7-acd1-2ea665e0db93.xml, winddi/PATHOBJ_bCloseFigure
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
 - PATHOBJ_bCloseFigure
 - winddi/PATHOBJ_bCloseFigure
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
 - PATHOBJ_bCloseFigure
---

# PATHOBJ_bCloseFigure function


## -description

The <b>PATHOBJ_bCloseFigure</b> function closes an open figure in a path by drawing a line from the current position to the first point of the figure.

## -parameters

### -param ppo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure that identifies the path to be closed.

## -returns

The return value is <b>TRUE</b> if the function is successful.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>