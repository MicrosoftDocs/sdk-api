---
UID: NF:d2d1helper.RectF
title: RectF function (d2d1helper.h)
description: Creates a D2D1_RECT_F structure that contains the specified dimensions.
helpviewer_keywords: ["RectF","RectF function [Direct2D]","d2d1helper/RectF","direct2d.rectf"]
old-location: direct2d\rectf.htm
tech.root: Direct2D
ms.assetid: 8abcc11d-40be-45ac-9f23-b94adf9842d5
ms.date: 12/05/2018
ms.keywords: RectF, RectF function [Direct2D], d2d1helper/RectF, direct2d.rectf
req.header: d2d1helper.h
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
 - RectF
 - d2d1helper/RectF
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
 - RectF
---

# RectF function


## -description

Creates a <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a> structure that contains the specified dimensions.

## -parameters

### -param left

Type: <b>FLOAT</b>

The x-coordinate of the upper-left corner of the rectangle. The default value is 0.f.

### -param top

Type: <b>FLOAT</b>

The y-coordinate of the upper-left corner of the rectangle. The default value is 0.f.

### -param right

Type: <b>FLOAT</b>

The x-coordinate of the lower-right corner of the rectangle. The default value is 0.f.

### -param bottom

Type: <b>FLOAT</b>

The y-coordinate of the lower-right corner of the rectangle. The default value is 0.f.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

A rectangle structure that contains the specified dimensions.