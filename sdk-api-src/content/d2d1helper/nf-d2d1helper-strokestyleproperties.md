---
UID: NF:d2d1helper.StrokeStyleProperties
title: StrokeStyleProperties function (d2d1helper.h)
description: Creates a D2D1_STROKE_STYLE_PROPERTIES structure.
helpviewer_keywords: ["StrokeStyleProperties","StrokeStyleProperties function [Direct2D]","d2d1helper/StrokeStyleProperties","direct2d.strokestyleproperties"]
old-location: direct2d\strokestyleproperties.htm
tech.root: Direct2D
ms.assetid: 7b7c2313-b105-45b2-9348-752ca44db716
ms.date: 12/05/2018
ms.keywords: StrokeStyleProperties, StrokeStyleProperties function [Direct2D], d2d1helper/StrokeStyleProperties, direct2d.strokestyleproperties
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
 - StrokeStyleProperties
 - d2d1helper/StrokeStyleProperties
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
 - StrokeStyleProperties
---

# StrokeStyleProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties">D2D1_STROKE_STYLE_PROPERTIES</a> structure.

## -parameters

### -param startCap

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The shape at the beginning of a stroke. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE_FLAT</a>.

### -param endCap

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The shape at the end of a stroke. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE_FLAT</a>.

### -param dashCap

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The shape  at either end of each dash segment. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE_FLAT</a>.

### -param lineJoin

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_line_join">D2D1_LINE_JOIN</a></b>

A value that describes how segments are joined. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_line_join">D2D1_LINE_JOIN_MITER</a>.

### -param miterLimit

Type: <b>FLOAT</b>

The limit of the thickness of the join on a mitered corner. This value is always treated as though it is greater than or equal to 1.0f.

The default value is 10.0f.

### -param dashStyle

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style">D2D1_DASH_STYLE</a></b>

A value that specifies whether the stroke has a dash pattern and, if so, the dash style. 

The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style">D2D1_DASH_STYLE_SOLID</a>.

### -param dashOffset

Type: <b>FLOAT</b>

A value that specifies how far in the dash sequence the stroke will start. 

The default value is 0.0f.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties">D2D1_STROKE_STYLE_PROPERTIES</a></b>

The new stroke style.