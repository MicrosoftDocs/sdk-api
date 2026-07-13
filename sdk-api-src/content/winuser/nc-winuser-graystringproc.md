---
UID: NC:winuser.GRAYSTRINGPROC
title: GRAYSTRINGPROC (winuser.h)
description: The OutputProc function is an application-defined callback function used with the GrayString function.
helpviewer_keywords: ["GRAYSTRINGPROC","GRAYSTRINGPROC callback","GRAYSTRINGPROC callback function [Windows GDI]","_win32_OutputProc","gdi.outputproc","winuser/GRAYSTRINGPROC"]
old-location: gdi\outputproc.htm
tech.root: gdi
ms.assetid: 4d9145d2-5be4-4da3-9d03-01ebd74e0d06
ms.date: 09/30/2025
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

An application-defined callback function used with the [GrayString](/windows/desktop/api/winuser/nf-winuser-graystringa) function. It is used to draw a string. The **GRAYSTRINGPROC** type defines a pointer to this callback function. _GrayStringProc_ (or _OutputProc_) is a placeholder for the application-defined or library-defined function name.

## -parameters

### -param unnamedParam1

Type: **HDC**

A handle to a device context with a bitmap of at least the width and height specified by the _nWidth_ and _nHeight_ parameters passed to [GrayString](/windows/desktop/api/winuser/nf-winuser-graystringa). This parameter is typically named _hDc_.

### -param unnamedParam2

Type: **LPARAM**

A pointer to the string to be drawn. This parameter is typically named _lpData_.

### -param unnamedParam3

Type: **int**

The length, in characters, of the string. This parameter is typically named _nCount_.

## -returns

Type: **BOOL**

If it succeeds, the callback function should return **TRUE**.

If the function fails, the return value is **FALSE**.

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef BOOL (CALLBACK* GRAYSTRINGPROC)(HDC, LPARAM, int);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam3`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

The callback function must draw an image relative to the coordinates (0,0).

## -see-also

[GrayString](/windows/desktop/api/winuser/nf-winuser-graystringa)

[Painting and Drawing Functions](/windows/desktop/gdi/painting-and-drawing-functions)

[Painting and Drawing Overview](/windows/desktop/gdi/painting-and-drawing)