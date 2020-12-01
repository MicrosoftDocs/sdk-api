---
UID: NF:wingdi.CombineTransform
title: CombineTransform function (wingdi.h)
description: The CombineTransform function concatenates two world-space to page-space transformations.
helpviewer_keywords: ["CombineTransform","CombineTransform function [Windows GDI]","_win32_CombineTransform","gdi.combinetransform","wingdi/CombineTransform"]
old-location: gdi\combinetransform.htm
tech.root: gdi
ms.assetid: 6ccd7828-7aa6-4c86-a340-b93e50cf3a2a
ms.date: 12/05/2018
ms.keywords: CombineTransform, CombineTransform function [Windows GDI], _win32_CombineTransform, gdi.combinetransform, wingdi/CombineTransform
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
 - CombineTransform
 - wingdi/CombineTransform
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
 - CombineTransform
---

# CombineTransform function


## -description

The <b>CombineTransform</b> function concatenates two world-space to page-space transformations.

## -parameters

### -param lpxfOut [out]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure that receives the combined transformation.

### -param lpxf1 [in]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure that specifies the first transformation.

### -param lpxf2 [in]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure that specifies the second transformation.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Applying the combined transformation has the same effect as applying the first transformation and then applying the second transformation.

The three transformations need not be distinct. For example, <i>lpxform1</i> can point to the same <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure as <i>lpxformResult</i>.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getworldtransform">GetWorldTransform</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a>