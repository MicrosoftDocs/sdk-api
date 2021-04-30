---
UID: NC:winuser.GRAYSTRINGPROC
title: GRAYSTRINGPROC (winuser.h)
description: The OutputProc function is an application-defined callback function used with the GrayString function.
helpviewer_keywords: ["GRAYSTRINGPROC","GRAYSTRINGPROC callback","GRAYSTRINGPROC callback function [Windows GDI]","_win32_OutputProc","gdi.outputproc","winuser/GRAYSTRINGPROC"]
old-location: gdi\outputproc.htm
tech.root: gdi
ms.assetid: 4d9145d2-5be4-4da3-9d03-01ebd74e0d06
ms.date: 12/05/2018
ms.keywords: GRAYSTRINGPROC, GRAYSTRINGPROC callback, GRAYSTRINGPROC callback function [Windows GDI], _win32_OutputProc, gdi.outputproc, winuser/GRAYSTRINGPROC
req.header: winuser.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GRAYSTRINGPROC
 - winuser/GRAYSTRINGPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - GRAYSTRINGPROC
---

# GRAYSTRINGPROC callback function


## -description

The <b>OutputProc</b> function is an application-defined callback function used with the <a href="/windows/desktop/api/winuser/nf-winuser-graystringa">GrayString</a> function. It is used to draw a string. The <b>GRAYSTRINGPROC</b> type defines a pointer to this callback function. <b>OutputProc</b> is a placeholder for the application-defined or library-defined function name.

## -parameters

### -param unnamedParam1

A handle to a device context with a bitmap of at least the width and height specified by the <i>nWidth</i> and <i>nHeight</i> parameters passed to <a href="/windows/desktop/api/winuser/nf-winuser-graystringa">GrayString</a>.

### -param unnamedParam2

A pointer to the string to be drawn.

### -param unnamedParam3

The length, in characters, of the string.

## -returns

If it succeeds, the callback function should return <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

The callback function must draw an image relative to the coordinates (0,0).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-graystringa">GrayString</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>