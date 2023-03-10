---
UID: NF:wingdi.PathToRegion
title: PathToRegion function (wingdi.h)
description: The PathToRegion function creates a region from the path that is selected into the specified device context. The resulting region uses device coordinates.
helpviewer_keywords: ["PathToRegion","PathToRegion function [Windows GDI]","_win32_PathToRegion","gdi.pathtoregion","wingdi/PathToRegion"]
old-location: gdi\pathtoregion.htm
tech.root: gdi
ms.assetid: 9fe31925-3d5d-42e5-aa9b-405610f13de4
ms.date: 12/05/2018
ms.keywords: PathToRegion, PathToRegion function [Windows GDI], _win32_PathToRegion, gdi.pathtoregion, wingdi/PathToRegion
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
 - PathToRegion
 - wingdi/PathToRegion
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
 - PathToRegion
---

# PathToRegion function


## -description

The <b>PathToRegion</b> function creates a region from the path that is selected into the specified device context. The resulting region uses device coordinates.

## -parameters

### -param hdc [in]

Handle to a device context that contains a closed path.

## -returns

If the function succeeds, the return value identifies a valid region.

If the function fails, the return value is zero.

## -remarks

When you no longer need the <b>HRGN</b> object call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

The device context identified by the <i>hdc</i> parameter must contain a closed path.

After <b>PathToRegion</b> converts a path into a region, the system discards the closed path from the specified device context.