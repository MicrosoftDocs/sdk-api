---
UID: NF:wingdi.EndPath
title: EndPath function (wingdi.h)
description: The EndPath function closes a path bracket and selects the path defined by the bracket into the specified device context.
helpviewer_keywords: ["EndPath","EndPath function [Windows GDI]","_win32_EndPath","gdi.endpath","wingdi/EndPath"]
old-location: gdi\endpath.htm
tech.root: gdi
ms.assetid: 0b4daf81-d1d6-45c1-b081-855b7cd8527a
ms.date: 12/05/2018
ms.keywords: EndPath, EndPath function [Windows GDI], _win32_EndPath, gdi.endpath, wingdi/EndPath
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
 - EndPath
 - wingdi/EndPath
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
 - EndPath
---

# EndPath function


## -description

The <b>EndPath</b> function closes a path bracket and selects the path defined by the bracket into the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context into which the new path is selected.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>