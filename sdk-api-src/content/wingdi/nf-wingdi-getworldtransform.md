---
UID: NF:wingdi.GetWorldTransform
title: GetWorldTransform function (wingdi.h)
description: The GetWorldTransform function retrieves the current world-space to page-space transformation.
helpviewer_keywords: ["GetWorldTransform","GetWorldTransform function [Windows GDI]","_win32_GetWorldTransform","gdi.getworldtransform","wingdi/GetWorldTransform"]
old-location: gdi\getworldtransform.htm
tech.root: gdi
ms.assetid: 72945b1e-144e-4724-bf08-6f971f8adb43
ms.date: 12/05/2018
ms.keywords: GetWorldTransform, GetWorldTransform function [Windows GDI], _win32_GetWorldTransform, gdi.getworldtransform, wingdi/GetWorldTransform
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
 - GetWorldTransform
 - wingdi/GetWorldTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetWorldTransform
---

# GetWorldTransform function


## -description

The <b>GetWorldTransform</b> function retrieves the current world-space to page-space transformation.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpxf [out]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure that receives the current world-space to page-space transformation.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The precision of the transformation may be altered if an application calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a> function prior to calling <b>GetWorldTransform</b>. (This is because the internal format for storing transformation values uses a higher precision than a <b>FLOAT</b> value.)

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a>