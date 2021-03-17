---
UID: NF:d2d1_1helper.StrokeStyleProperties1
title: StrokeStyleProperties1 function (d2d1_1helper.h)
description: Returns a filled D2D1_STROKE_STYLE_PROPERTIES1 structure.
helpviewer_keywords: ["StrokeStyleProperties1","StrokeStyleProperties1 function [Direct2D]","d2d1_1helper/StrokeStyleProperties1","direct2d.strokestyleproperties1"]
old-location: direct2d\strokestyleproperties1.htm
tech.root: Direct2D
ms.assetid: 12D8FBEF-2FB5-4846-857D-6D6B230DE837
ms.date: 12/05/2018
ms.keywords: StrokeStyleProperties1, StrokeStyleProperties1 function [Direct2D], d2d1_1helper/StrokeStyleProperties1, direct2d.strokestyleproperties1
req.header: d2d1_1helper.h
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
 - StrokeStyleProperties1
 - d2d1_1helper/StrokeStyleProperties1
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
 - StrokeStyleProperties1
---

# StrokeStyleProperties1 function


## -description

Returns a filled D2D1_STROKE_STYLE_PROPERTIES1 structure.

## -parameters

### -param startCap

The cap to use at the start of each open figure.

### -param endCap

The cap to use at the end of each open figure.

### -param dashCap

The cap to use at the start and end of each dash.

### -param lineJoin

The line join to use.

### -param miterLimit

The limit beyond which miters are either clamped or converted to bevels.

### -param dashStyle

The type of dash to use.

### -param dashOffset

The location of the first dash, relative to the start of the figure.

### -param transformType

The rule that determines what render target properties affect the nib of the stroke.

## -returns

Describes the stroke that outlines a shape.

