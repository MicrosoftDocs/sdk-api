---
UID: NF:d2d1helper.Point2F
title: Point2F function (d2d1helper.h)
description: Creates a D2D1_POINT_2F structure that contains the specified x-coordinates and y-coordinates.
helpviewer_keywords: ["Point2F","Point2F function [Direct2D]","d2d1helper/Point2F","direct2d.point2f"]
old-location: direct2d\point2f.htm
tech.root: Direct2D
ms.assetid: 62eb7517-0c38-4f63-b9f9-85211fcb36a4
ms.date: 12/05/2018
ms.keywords: Point2F, Point2F function [Direct2D], d2d1helper/Point2F, direct2d.point2f
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
 - Point2F
 - d2d1helper/Point2F
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
 - Point2F
---

# Point2F function


## -description

Creates a <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a> structure that contains the specified x-coordinates and y-coordinates.

## -parameters

### -param x

Type: <b>FLOAT</b>

The x-coordinate of the point. The default value is 0.f.

### -param y

Type: <b>FLOAT</b>

The y-coordinate of the point. The default value is 0.f.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The new point.