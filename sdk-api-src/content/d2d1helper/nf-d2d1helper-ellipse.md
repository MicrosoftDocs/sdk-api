---
UID: NF:d2d1helper.Ellipse
title: Ellipse function (d2d1helper.h)
description: Creates a D2D1_ELLIPSE structure.
helpviewer_keywords: ["Ellipse","Ellipse function [Direct2D]","d2d1helper/Ellipse","direct2d.ellipse"]
old-location: direct2d\ellipse.htm
tech.root: Direct2D
ms.assetid: 49d1b737-acf3-4dd7-81ce-c78ac0558a87
ms.date: 12/05/2018
ms.keywords: Ellipse, Ellipse function [Direct2D], d2d1helper/Ellipse, direct2d.ellipse
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
 - Ellipse
 - d2d1helper/Ellipse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - Ellipse
---

# Ellipse function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse">D2D1_ELLIPSE</a> structure.

## -parameters

### -param center [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The center point of the ellipse.

### -param radiusX

Type: <b>FLOAT</b>

The x-radius of the ellipse.

### -param radiusY

Type: <b>FLOAT</b>

The y-radius of the ellipse.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse">D2D1_ELLIPSE</a></b>

The new ellipse.