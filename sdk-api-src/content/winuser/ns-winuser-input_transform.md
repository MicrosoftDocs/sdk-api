---
UID: NS:winuser.tagINPUT_TRANSFORM
title: INPUT_TRANSFORM (winuser.h)
description: Defines the matrix that represents a transform on a message consumer.
helpviewer_keywords: ["INPUT_TRANSFORM","INPUT_TRANSFORM structure [Windows and Messages]","_INPUT_TRANSFORM","inputmsg.input_transform","winuser/INPUT_TRANSFORM"]
old-location: inputmsg\input_transform.htm
tech.root: InputMsg
ms.assetid: DE6854F0-17D8-4E4B-97CB-A135910A300C
ms.date: 12/05/2018
ms.keywords: INPUT_TRANSFORM, INPUT_TRANSFORM structure [Windows and Messages], _INPUT_TRANSFORM, inputmsg.input_transform, winuser/INPUT_TRANSFORM
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: INPUT_TRANSFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagINPUT_TRANSFORM
 - winuser/tagINPUT_TRANSFORM
 - INPUT_TRANSFORM
 - winuser/INPUT_TRANSFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - INPUT_TRANSFORM
---

# INPUT_TRANSFORM structure


## -description

Defines the matrix that represents a transform on a message consumer. This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._11

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._12

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._13

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._14

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._21

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._22

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._23

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._24

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._31

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._32

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._33

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._34

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._41

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._42

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._43

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME._44

### -field DUMMYUNIONNAME.m

 




#### - ( unnamed struct )

A 4x4 matrix, represented as a linear sequence of fields.



#### _11

The first floating-point column value in the first row of the matrix.



#### _12

The second floating-point column value in the first row of the matrix.



#### _13

The third floating-point column value in the first row of the matrix.



#### _14

The fourth floating-point column value in the first row of the matrix.



#### _21

The first floating-point column value in the second row of the matrix.



#### _22

The second floating-point column value in the second row of the matrix.



#### _23

The third floating-point column value in the second row of the matrix.



#### _24

The fourth floating-point column value in the second row of the matrix.



#### _31

The first floating-point column value in the third row of the matrix.



#### _32

The second floating-point column value in the third row of the matrix.



#### _33

The third floating-point column value in the third row of the matrix.



#### _34

The fourth floating-point column value in the third row of the matrix.



#### _41

The first floating-point column value in the fourth row of the matrix.



#### _42

The second floating-point column value in the fourth row of the matrix.



#### _43

The third floating-point column value in the fourth row of the matrix.



#### _44

The fourth floating-point column value in the fourth row of the matrix.


#### - m[4][4]

A 4x4 matrix, represented as a two-dimensional array.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getpointerinputtransform">GetPointerInputTransform</a>



<a href="/windows/win32/inputmsg/structures">Structures</a>