---
UID: NF:d2d1_1helper.RectL
title: RectL function (d2d1_1helper.h)
description: Returns a filled D2D1_RECT_L structure.
helpviewer_keywords: ["RectL","RectL function [Direct2D]","dciddi/RectL","direct2d.rectl"]
old-location: direct2d\rectl.htm
tech.root: Direct2D
ms.assetid: CE2B4034-24BC-49AE-88C6-C60BDCEA38B5
ms.date: 12/05/2018
ms.keywords: RectL, RectL function [Direct2D], dciddi/RectL, direct2d.rectl
req.header: d2d1_1helper.h
req.include-header: D2d1_1helper.h
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
 - RectL
 - d2d1_1helper/RectL
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
 - RectL
---

# RectL function


## -description

Returns a filled D2D1_RECT_L structure.

## -parameters

### -param left

Type: <b>INT32</b>

The x-coordinate of the upper-left corner of the rectangle.

### -param top

Type: <b>INT32</b>

The y-coordinate of the upper-left corner of the rectangle.

### -param right

Type: <b>INT32</b>

The x-coordinate of the lower-right corner of the rectangle.

### -param bottom

Type: <b>INT32</b>

The y-coordinate of the lower-right corner of the rectangle.

## -returns

Type: <b><a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a></b>

The RECT structure defines the coordinates of the upper-left and lower-right corners of a rectangle.