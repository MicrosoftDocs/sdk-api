---
UID: NF:wingdi.FillPath
title: FillPath function (wingdi.h)
description: The FillPath function closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.
helpviewer_keywords: ["FillPath","FillPath function [Windows GDI]","_win32_FillPath","gdi.fillpath","wingdi/FillPath"]
old-location: gdi\fillpath.htm
tech.root: gdi
ms.assetid: a80b299a-c3f9-411b-9936-33d32fc71853
ms.date: 12/05/2018
ms.keywords: FillPath, FillPath function [Windows GDI], _win32_FillPath, gdi.fillpath, wingdi/FillPath
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
 - FillPath
 - wingdi/FillPath
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
 - FillPath
---

# FillPath function


## -description

The <b>FillPath</b> function closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.

## -parameters

### -param hdc [in]

A handle to a device context that contains a valid path.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

After its interior is filled, the path is discarded from the DC identified by the <i>hdc</i> parameter.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-strokeandfillpath">StrokeAndFillPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-strokepath">StrokePath</a>