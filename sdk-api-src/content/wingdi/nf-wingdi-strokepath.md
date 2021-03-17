---
UID: NF:wingdi.StrokePath
title: StrokePath function (wingdi.h)
description: The StrokePath function renders the specified path by using the current pen.
helpviewer_keywords: ["StrokePath","StrokePath function [Windows GDI]","_win32_StrokePath","gdi.strokepath","wingdi/StrokePath"]
old-location: gdi\strokepath.htm
tech.root: gdi
ms.assetid: 5a9f1509-0a69-4db8-8d74-9bf360aca64d
ms.date: 12/05/2018
ms.keywords: StrokePath, StrokePath function [Windows GDI], _win32_StrokePath, gdi.strokepath, wingdi/StrokePath
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrokePath
 - wingdi/StrokePath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
api_name:
 - StrokePath
---

# StrokePath function


## -description

The <b>StrokePath</b> function renders the specified path by using the current pen.

## -parameters

### -param hdc [in]

Handle to a device context that contains the completed path.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The path, if it is to be drawn by <b>StrokePath</b>, must have been completed through a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>. Calling this function on a path for which <b>EndPath</b> has not been called will cause this function to fail and return zero.  Unlike other path drawing functions such as <a href="/windows/desktop/api/wingdi/nf-wingdi-strokeandfillpath">StrokeAndFillPath</a>, <b>StrokePath</b> will not attempt to close the path by drawing a straight line from the first point on the path to the last point on the path.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>