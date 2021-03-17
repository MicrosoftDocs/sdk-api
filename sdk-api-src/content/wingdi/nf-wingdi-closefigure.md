---
UID: NF:wingdi.CloseFigure
title: CloseFigure function (wingdi.h)
description: The CloseFigure function closes an open figure in a path.
helpviewer_keywords: ["CloseFigure","CloseFigure function [Windows GDI]","_win32_CloseFigure","gdi.closefigure","wingdi/CloseFigure"]
old-location: gdi\closefigure.htm
tech.root: gdi
ms.assetid: 2532227c-35c9-4a46-b4eb-4a156ef28219
ms.date: 12/05/2018
ms.keywords: CloseFigure, CloseFigure function [Windows GDI], _win32_CloseFigure, gdi.closefigure, wingdi/CloseFigure
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
 - CloseFigure
 - wingdi/CloseFigure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Path-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - CloseFigure
---

# CloseFigure function


## -description

The <b>CloseFigure</b> function closes an open figure in a path.

## -parameters

### -param hdc [in]

Handle to the device context in which the figure will be closed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>CloseFigure</b> function closes the figure by drawing a line from the current position to the first point of the figure (usually, the point specified by the most recent call to the <a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a> function) and then connects the lines by using the line join style. If a figure is closed by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a> function instead of <b>CloseFigure</b>, end caps are used to create the corner instead of a join.

The <b>CloseFigure</b> function should only be called if there is an open path bracket in the specified device context.

A figure in a path is open unless it is explicitly closed by using this function. (A figure can be open even if the current point and the starting point of the figure are the same.)

After a call to <b>CloseFigure</b>, adding a line or curve to the path starts a new figure.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>