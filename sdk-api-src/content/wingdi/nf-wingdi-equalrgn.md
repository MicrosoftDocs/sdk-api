---
UID: NF:wingdi.EqualRgn
title: EqualRgn function (wingdi.h)
description: The EqualRgn function checks the two specified regions to determine whether they are identical. The function considers two regions identical if they are equal in size and shape.
helpviewer_keywords: ["EqualRgn","EqualRgn function [Windows GDI]","_win32_EqualRgn","gdi.equalrgn","wingdi/EqualRgn"]
old-location: gdi\equalrgn.htm
tech.root: gdi
ms.assetid: c7829998-78f4-4334-bf34-92aad12555f5
ms.date: 12/05/2018
ms.keywords: EqualRgn, EqualRgn function [Windows GDI], _win32_EqualRgn, gdi.equalrgn, wingdi/EqualRgn
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
 - EqualRgn
 - wingdi/EqualRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - EqualRgn
---

# EqualRgn function


## -description

The <b>EqualRgn</b> function checks the two specified regions to determine whether they are identical. The function considers two regions identical if they are equal in size and shape.

## -parameters

### -param hrgn1 [in]

Handle to a region.

### -param hrgn2 [in]

Handle to a region.

## -returns

If the two regions are equal, the return value is nonzero.

If the two regions are not equal, the return value is zero. A return value of ERROR means at least one of the region handles is invalid.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>