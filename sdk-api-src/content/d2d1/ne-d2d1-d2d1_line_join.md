---
UID: NE:d2d1.D2D1_LINE_JOIN
title: D2D1_LINE_JOIN (d2d1.h)
description: Describes the shape that joins two lines or segments.
helpviewer_keywords: ["D2D1_LINE_JOIN","D2D1_LINE_JOIN enumeration [Direct2D]","D2D1_LINE_JOIN_BEVEL","D2D1_LINE_JOIN_MITER","D2D1_LINE_JOIN_MITER_OR_BEVEL","D2D1_LINE_JOIN_ROUND","d2d1/D2D1_LINE_JOIN","d2d1/D2D1_LINE_JOIN_BEVEL","d2d1/D2D1_LINE_JOIN_MITER","d2d1/D2D1_LINE_JOIN_MITER_OR_BEVEL","d2d1/D2D1_LINE_JOIN_ROUND","direct2d.D2D1_LINE_JOIN"]
old-location: direct2d\D2D1_LINE_JOIN.htm
tech.root: Direct2D
ms.assetid: 4368e93e-af69-4555-ac2b-c9c576c81372
ms.date: 12/05/2018
ms.keywords: D2D1_LINE_JOIN, D2D1_LINE_JOIN enumeration [Direct2D], D2D1_LINE_JOIN_BEVEL, D2D1_LINE_JOIN_MITER, D2D1_LINE_JOIN_MITER_OR_BEVEL, D2D1_LINE_JOIN_ROUND, d2d1/D2D1_LINE_JOIN, d2d1/D2D1_LINE_JOIN_BEVEL, d2d1/D2D1_LINE_JOIN_MITER, d2d1/D2D1_LINE_JOIN_MITER_OR_BEVEL, d2d1/D2D1_LINE_JOIN_ROUND, direct2d.D2D1_LINE_JOIN
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_LINE_JOIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_LINE_JOIN
 - d2d1/D2D1_LINE_JOIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_LINE_JOIN
---

# D2D1_LINE_JOIN enumeration


## -description

Describes the shape that joins two lines or segments.

## -enum-fields

### -field D2D1_LINE_JOIN_MITER:0

Regular angular vertices.

### -field D2D1_LINE_JOIN_BEVEL:1

Beveled vertices.

### -field D2D1_LINE_JOIN_ROUND:2

Rounded vertices.

### -field D2D1_LINE_JOIN_MITER_OR_BEVEL:3

Regular angular vertices unless the join would extend beyond the miter limit; otherwise, beveled vertices.

### -field D2D1_LINE_JOIN_FORCE_DWORD:0xffffffff

## -remarks

A miter limit affects how sharp miter joins are allowed to be.
	If the line join style is <b>D2D1_LINE_JOIN_MITER_OR_BEVEL</b>, then the join will be mitered with regular angular vertices if it doesn't extend
	beyond the miter limit; otherwise, the line join will be beveled.

The following illustration shows  different line join settings for the same stroked path geometry.  

<img alt="Illustration of line join settings" src="./images/StrokeStyle_Join.png"/>

