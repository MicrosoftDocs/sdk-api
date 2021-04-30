---
UID: NF:wingdi.FlattenPath
title: FlattenPath function (wingdi.h)
description: The FlattenPath function transforms any curves in the path that is selected into the current device context (DC), turning each curve into a sequence of lines.
helpviewer_keywords: ["FlattenPath","FlattenPath function [Windows GDI]","_win32_FlattenPath","gdi.flattenpath","wingdi/FlattenPath"]
old-location: gdi\flattenpath.htm
tech.root: gdi
ms.assetid: 267b0c9a-25d4-4b04-95d3-6b0856bed022
ms.date: 12/05/2018
ms.keywords: FlattenPath, FlattenPath function [Windows GDI], _win32_FlattenPath, gdi.flattenpath, wingdi/FlattenPath
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
 - FlattenPath
 - wingdi/FlattenPath
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
 - FlattenPath
---

# FlattenPath function


## -description

The <b>FlattenPath</b> function transforms any curves in the path that is selected into the current device context (DC), turning each curve into a sequence of lines.

## -parameters

### -param hdc [in]

A handle to a DC that contains a valid path.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-widenpath">WidenPath</a>