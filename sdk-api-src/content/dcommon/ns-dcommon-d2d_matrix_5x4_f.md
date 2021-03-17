---
UID: NS:dcommon.D2D_MATRIX_5X4_F
title: D2D_MATRIX_5X4_F (dcommon.h)
description: Describes a 5-by-4 floating point matrix.
helpviewer_keywords: ["D2D_MATRIX_5X4_F","D2D_MATRIX_5X4_F structure [Direct2D]","dcommon/D2D_MATRIX_5X4_F","direct2d.d2d_matrix_5x4_f"]
old-location: direct2d\d2d_matrix_5x4_f.htm
tech.root: Direct2D
ms.assetid: E7161468-82F4-4DAC-B376-FFB96293F634
ms.date: 12/05/2018
ms.keywords: D2D_MATRIX_5X4_F, D2D_MATRIX_5X4_F structure [Direct2D], dcommon/D2D_MATRIX_5X4_F, direct2d.d2d_matrix_5x4_f
f1_keywords:
- dcommon/D2D_MATRIX_5X4_F
dev_langs:
- c++
req.header: dcommon.h
req.include-header: D2d1.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dcommon.h
api_name:
- D2D_MATRIX_5X4_F
targetos: Windows
req.typenames: D2D_MATRIX_5X4_F
req.redist: 
ms.custom: 19H1
---

## -description

Describes a 5-by-4 floating point matrix.

## -struct-fields

### -field _11

Type: <b>FLOAT</b>

The value in the first row and first column of the matrix.

### -field _12

Type: <b>FLOAT</b>

The value in the first row and second column of the matrix.

### -field _13

Type: <b>FLOAT</b>

The value in the first row and third column of the matrix.

### -field _14

Type: <b>FLOAT</b>

The value in the first row and fourth column of the matrix.

### -field _15

Type: <b>FLOAT</b>

The value in the first row and fifth column of the matrix.

### -field _21

Type: <b>FLOAT</b>

The value in the second row and first column of the matrix.

### -field _22

Type: <b>FLOAT</b>

The value in the second row and second column of the matrix.

### -field _23

Type: <b>FLOAT</b>

The value in the second row and third column of the matrix.

### -field _24

Type: <b>FLOAT</b>

The value in the second row and fourth column of the matrix.

### -field _25

Type: <b>FLOAT</b>

The value in the second row and fifth column of the matrix.

### -field _31

Type: <b>FLOAT</b>

The value in the third row and first column of the matrix.

### -field _32

Type: <b>FLOAT</b>

The value in the third row and second column of the matrix.

### -field _33

Type: <b>FLOAT</b>

The value in the third row and third column of the matrix.

### -field _34

Type: <b>FLOAT</b>

The value in the third row and fourth column of the matrix.

### -field _35

Type: <b>FLOAT</b>

The value in the third row and fifth column of the matrix.

### -field _41

Type: <b>FLOAT</b>

The value in the fourth row and first column of the matrix.

### -field _42

Type: <b>FLOAT</b>

The value in the fourth row and second column of the matrix.

### -field _43

Type: <b>FLOAT</b>

The value in the fourth row and third column of the matrix.

### -field _44

Type: <b>FLOAT</b>

The value in the fourth row and fourth column of the matrix.

### -field _45

Type: <b>FLOAT</b>

The value in the fourth row and fifth column of the matrix.

### -field m

A 5-by-4 floating point array that describes the matrix.

## -remarks

The <b>D2D1_MATRIX_5X4_F</b> structure is type defined from a <b>D2D_MATRIX_5X4_F</b> structure in D2d1_1.h.

```cpp
typedef D2D_MATRIX_5X4_F D2D1_MATRIX_5X4_F;
```