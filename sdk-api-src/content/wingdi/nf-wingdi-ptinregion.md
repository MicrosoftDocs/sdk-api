---
UID: NF:wingdi.PtInRegion
title: PtInRegion function (wingdi.h)
description: The PtInRegion function determines whether the specified point is inside the specified region.
helpviewer_keywords: ["PtInRegion","PtInRegion function [Windows GDI]","_win32_PtInRegion","gdi.ptinregion","wingdi/PtInRegion"]
old-location: gdi\ptinregion.htm
tech.root: gdi
ms.assetid: 6fab6126-4672-49d6-825b-66a7927a7e99
ms.date: 12/05/2018
ms.keywords: PtInRegion, PtInRegion function [Windows GDI], _win32_PtInRegion, gdi.ptinregion, wingdi/PtInRegion
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
 - PtInRegion
 - wingdi/PtInRegion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - PtInRegion
---

# PtInRegion function


## -description

The <b>PtInRegion</b> function determines whether the specified point is inside the specified region.

## -parameters

### -param hrgn [in]

Handle to the region to be examined.

### -param x [in]

Specifies the x-coordinate of the point in logical units.

### -param y [in]

Specifies the y-coordinate of the point in logical units.

## -returns

If the specified point is in the region, the return value is nonzero.

If the specified point is not in the region, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-rectinregion">RectInRegion</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>