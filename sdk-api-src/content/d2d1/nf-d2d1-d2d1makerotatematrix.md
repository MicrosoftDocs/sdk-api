---
UID: NF:d2d1.D2D1MakeRotateMatrix
title: D2D1MakeRotateMatrix function (d2d1.h)
description: Creates a rotation transformation that rotates by the specified angle about the specified point.
helpviewer_keywords: ["D2D1MakeRotateMatrix","D2D1MakeRotateMatrix function [Direct2D]","d2d1/D2D1MakeRotateMatrix","direct2d.d2d1makerotatematrix"]
old-location: direct2d\d2d1makerotatematrix.htm
tech.root: Direct2D
ms.assetid: 5e066328-5b0f-4e7a-9bf4-df55521fcc2b
ms.date: 12/05/2018
ms.keywords: D2D1MakeRotateMatrix, D2D1MakeRotateMatrix function [Direct2D], d2d1/D2D1MakeRotateMatrix, direct2d.d2d1makerotatematrix
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1MakeRotateMatrix
 - d2d1/D2D1MakeRotateMatrix
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
 - D2D1MakeRotateMatrix
---

# D2D1MakeRotateMatrix function


## -description

Creates a rotation transformation that rotates by the specified angle about the specified point.

## -parameters

### -param angle [in]

Type: <b>FLOAT</b>

The clockwise rotation angle, in degrees.

### -param center [in]

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point about which to rotate.

### -param matrix [out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains the new rotation transformation. You must allocate storage for this parameter.

## -remarks

Rotation occurs in the plane of the 2-D surface.

