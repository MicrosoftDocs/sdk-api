---
UID: NF:d2d1_3helper.InkPoint
title: InkPoint function (d2d1_3helper.h)
description: Creates a D2D1_INK_POINT structure.
helpviewer_keywords: ["InkPoint","InkPoint function [Direct2D]","d2d1_3helper/InkPoint","direct2d.inkpoint"]
old-location: direct2d\inkpoint.htm
tech.root: Direct2D
ms.assetid: 6ab8c30d-1ab8-1148-5cce-29797c5f5ad5
ms.date: 12/05/2018
ms.keywords: InkPoint, InkPoint function [Direct2D], d2d1_3helper/InkPoint, direct2d.inkpoint
req.header: d2d1_3helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkPoint
 - d2d1_3helper/InkPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - InkPoint
---

# InkPoint function


## -description

Creates a <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a> structure.

## -parameters

### -param point [ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The x and y coordinates of the point.

### -param radius

Type: <b>FLOAT</b>

The radius of this point. Corresponds to the width of the ink stroke at this point in the stroke.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a></b>

Returns the created <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a> structure.

## -see-also

<a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a>