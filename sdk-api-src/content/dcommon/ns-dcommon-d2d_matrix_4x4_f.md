---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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


