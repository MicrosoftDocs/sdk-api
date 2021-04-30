---
UID: NF:d2d1_3helper.InkStyleProperties
title: InkStyleProperties function (d2d1_3helper.h)
description: Creates a D2D1_INK_STYLE_PROPERTIES structure.
helpviewer_keywords: ["InkStyleProperties","InkStyleProperties function [Direct2D]","d2d1_3helper/InkStyleProperties","direct2d.inkstyleproperties"]
old-location: direct2d\inkstyleproperties.htm
tech.root: Direct2D
ms.assetid: a923ce8e-71a0-6332-13e1-a4d58750d1ff
ms.date: 12/05/2018
ms.keywords: InkStyleProperties, InkStyleProperties function [Direct2D], d2d1_3helper/InkStyleProperties, direct2d.inkstyleproperties
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
 - InkStyleProperties
 - d2d1_3helper/InkStyleProperties
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
 - InkStyleProperties
---

# InkStyleProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties">D2D1_INK_STYLE_PROPERTIES</a> structure.

## -parameters

### -param nibShape

Type: <b><a href="/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_ink_nib_shape">D2D1_INK_NIB_SHAPE</a></b>

The pre-transform shape of the nib (pen tip) used to draw a given ink object.

### -param nibTransform [ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transform applied to the nib. Note that the translation components of the transform matrix are ignored for the purposes of rendering.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties">D2D1_INK_STYLE_PROPERTIES</a></b>

Returns the created <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties">D2D1_INK_STYLE_PROPERTIES</a> structure.

## -see-also

<a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties">D2D1_INK_STYLE_PROPERTIES</a>