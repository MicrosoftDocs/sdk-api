---
UID: NF:d2d1helper.RectU
title: RectU function (d2d1helper.h)
description: Creates a D2D1_RECT_U structure that contains the specified dimensions.
helpviewer_keywords: ["RectU","RectU function [Direct2D]","d2d1helper/RectU","direct2d.rectu"]
old-location: direct2d\rectu.htm
tech.root: Direct2D
ms.assetid: a0b7b850-b58d-43a0-b5c5-61a3791f0681
ms.date: 12/05/2018
ms.keywords: RectU, RectU function [Direct2D], d2d1helper/RectU, direct2d.rectu
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
 - RectU
 - d2d1helper/RectU
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
 - RectU
---

# RectU function


## -description

Creates a <a href="/windows/desktop/Direct2D/d2d1-rect-u">D2D1_RECT_U</a> structure that contains the specified dimensions.

## -parameters

### -param left

Type: <b>UINT32</b>

The x-coordinate of the upper-left corner of the rectangle. The default value is 0.

### -param top

Type: <b>UINT32</b>

The y-coordinate of the upper-left corner of the rectangle. The default value is 0.

### -param right

Type: <b>UINT32</b>

The x-coordinate of the lower-right corner of the rectangle. The default value is 0.

### -param bottom

Type: <b>UINT32</b>

The y-coordinate of the lower-right corner of the rectangle. The default value is 0.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-u">D2D1_RECT_U</a></b>

A rectangle structure that contains the specified dimensions.