---
UID: NF:wingdi.WidenPath
title: WidenPath function (wingdi.h)
description: The WidenPath function redefines the current path as the area that would be painted if the path were stroked using the pen currently selected into the given device context.
helpviewer_keywords: ["WidenPath","WidenPath function [Windows GDI]","_win32_WidenPath","gdi.widenpath","wingdi/WidenPath"]
old-location: gdi\widenpath.htm
tech.root: gdi
ms.assetid: c994bd1b-c5e8-46e6-a6a6-59e2d9106d75
ms.date: 12/05/2018
ms.keywords: WidenPath, WidenPath function [Windows GDI], _win32_WidenPath, gdi.widenpath, wingdi/WidenPath
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
 - WidenPath
 - wingdi/WidenPath
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
 - GDI32Full.dll
api_name:
 - WidenPath
---

# WidenPath function


## -description

The <b>WidenPath</b> function redefines the current path as the area that would be painted if the path were stroked using the pen currently selected into the given device context.

## -parameters

### -param hdc [in]

A handle to a device context that contains a closed path.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>WidenPath</b> function is successful only if the current pen is a geometric pen created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a> function, or if the pen is created with the <a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a> function and has a width, in device units, of more than one.

The device context identified by the <i>hdc</i> parameter must contain a closed path.

Any Bézier curves in the path are converted to sequences of straight lines approximating the widened curves. As such, no Bézier curves remain in the path after <b>WidenPath</b> is called.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmiterlimit">SetMiterLimit</a>