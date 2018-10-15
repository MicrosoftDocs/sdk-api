---
UID: NS:dcommon.D2D_MATRIX_4X4_F
title: D2D_MATRIX_4X4_F
author: windows-sdk-content
description: Describes a 4-by-4 floating point matrix.
old-location: direct2d\d2d_matrix_4x4_f.htm
tech.root: direct2d
ms.assetid: 7355F5EB-BC23-42AE-A1F2-3E5582A3156E
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: D2D_MATRIX_4X4_F, D2D_MATRIX_4X4_F structure [Direct2D], dcommon/D2D_MATRIX_4X4_F, direct2d.d2d_matrix_4x4_f
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - D2D_MATRIX_4X4_F
product: Windows
targetos: Windows
req.typenames: D2D_MATRIX_4X4_F
req.redist: 
---

# D2D_MATRIX_4X4_F structure


## -description


Describes a 4-by-4 floating point matrix.


## -struct-fields




### -field _11

 


### -field _12

 


### -field _13

 


### -field _14

 


### -field _21

 


### -field _22

 


### -field _23

 


### -field _24

 


### -field _31

 


### -field _32

 


### -field _33

 


### -field _34

 


### -field _41

 


### -field _42

 


### -field _43

 


### -field _44

 


### -field m

A 4-by-4 floating point array that describes the matrix.


#### - _11, _12, _13, _14

 The values in the first row and first, second, third, and fourth columns of the matrix.


#### - _21, _22, _23, _24

The values in the second row  and first, second, third, and fourth columns of the matrix.


#### - _31, _32, _33, _34

The values in the third row  and first, second, third, and fourth columns of the matrix.


#### - _41, _42, _43, _44

The value in the fourth row  and first, second, third, and fourth columns of the matrix.


## -remarks



The <b>D2D1_MATRIX_4X4_F</b> structure is type defined from a <b>D2D_MATRIX_4X4_F</b> structure in D2d1_1.h.

<pre class="syntax" xml:space="preserve"><code>
typedef D2D_MATRIX_4X4_F D2D1_MATRIX_4X4_F;
</code></pre>


