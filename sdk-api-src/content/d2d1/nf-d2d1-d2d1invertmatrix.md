---
UID: NF:d2d1.D2D1InvertMatrix
title: D2D1InvertMatrix function (d2d1.h)
description: Tries to invert the specified matrix.
helpviewer_keywords: ["D2D1InvertMatrix","D2D1InvertMatrix function [Direct2D]","d2d1/D2D1InvertMatrix","direct2d.d2d1invertmatrix"]
old-location: direct2d\d2d1invertmatrix.htm
tech.root: Direct2D
ms.assetid: af01b6df-ada9-4e21-98f0-356b96d1017a
ms.date: 12/05/2018
ms.keywords: D2D1InvertMatrix, D2D1InvertMatrix function [Direct2D], d2d1/D2D1InvertMatrix, direct2d.d2d1invertmatrix
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
 - D2D1InvertMatrix
 - d2d1/D2D1InvertMatrix
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
 - D2D1InvertMatrix
---

# D2D1InvertMatrix function


## -description

Tries to invert the specified matrix.

## -parameters

### -param matrix [in, out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The matrix to invert.

## -returns

Type: <b>BOOL</b>

<b>true</b> if the matrix was inverted; otherwise, <b>false</b>.

