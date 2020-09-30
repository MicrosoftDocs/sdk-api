---
UID: NF:wingdi.AbortPath
title: AbortPath function (wingdi.h)
description: The AbortPath function closes and discards any paths in the specified device context.
helpviewer_keywords: ["AbortPath","AbortPath function [Windows GDI]","_win32_AbortPath","gdi.abortpath","wingdi/AbortPath"]
old-location: gdi\abortpath.htm
tech.root: gdi
ms.assetid: 49299a11-910b-40e0-b02e-80a244cfc978
ms.date: 12/05/2018
ms.keywords: AbortPath, AbortPath function [Windows GDI], _win32_AbortPath, gdi.abortpath, wingdi/AbortPath
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
 - AbortPath
 - wingdi/AbortPath
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
 - AbortPath
---

# AbortPath function


## -description

The <b>AbortPath</b> function closes and discards any paths in the specified device context.

## -parameters

### -param hdc [in]

Handle to the device context from which a path will be discarded.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If there is an open path bracket in the given device context, the path bracket is closed and the path is discarded. If there is a closed path in the device context, the path is discarded.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>