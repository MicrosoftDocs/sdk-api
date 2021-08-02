---
UID: NF:d2d1.D2D1MakeSkewMatrix
title: D2D1MakeSkewMatrix function (d2d1.h)
description: Creates a skew transformation that has the specified x-axis angle, y-axis angle, and center point.
helpviewer_keywords: ["D2D1MakeSkewMatrix","D2D1MakeSkewMatrix function [Direct2D]","d2d1/D2D1MakeSkewMatrix","direct2d.d2d1makeskewmatrix"]
old-location: direct2d\d2d1makeskewmatrix.htm
tech.root: Direct2D
ms.assetid: 9f29488c-37f0-4d53-9e3b-3b27e841c8b4
ms.date: 12/05/2018
ms.keywords: D2D1MakeSkewMatrix, D2D1MakeSkewMatrix function [Direct2D], d2d1/D2D1MakeSkewMatrix, direct2d.d2d1makeskewmatrix
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
 - D2D1MakeSkewMatrix
 - d2d1/D2D1MakeSkewMatrix
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
 - D2D1MakeSkewMatrix
---

# D2D1MakeSkewMatrix function


## -description

Creates a skew transformation that has the specified x-axis angle, y-axis angle, and center point.

## -parameters

### -param angleX [in]

Type: <b>FLOAT</b>

The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.

### -param angleY [in]

Type: <b>FLOAT</b>

The y-axis skew angle, which is measured in degrees counterclockwise from the x-axis.

### -param center [in]

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The center point of the skew operation.

### -param matrix [out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains the rotation transformation. You must allocate storage for this parameter.

