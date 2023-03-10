---
UID: NF:d2d1helper.RoundedRect
title: RoundedRect function (d2d1helper.h)
description: Creates a D2D1_ROUNDED_RECT structure.
helpviewer_keywords: ["RoundedRect","RoundedRect function [Direct2D]","d2d1helper/RoundedRect","direct2d.roundedrect"]
old-location: direct2d\roundedrect.htm
tech.root: Direct2D
ms.assetid: 200119a2-941c-493f-9e56-c9f306dc5322
ms.date: 12/05/2018
ms.keywords: RoundedRect, RoundedRect function [Direct2D], d2d1helper/RoundedRect, direct2d.roundedrect
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
 - RoundedRect
 - d2d1helper/RoundedRect
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
 - RoundedRect
---

# RoundedRect function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect">D2D1_ROUNDED_RECT</a> structure.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The size and position of the rectangle.

### -param radiusX

Type: <b>FLOAT</b>

The x-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.

### -param radiusY

Type: <b>FLOAT</b>

The y-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect">D2D1_ROUNDED_RECT</a></b>

The new rounded rectangle.