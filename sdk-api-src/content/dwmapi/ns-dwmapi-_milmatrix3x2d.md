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

# _MilMatrix3x2D structure


## -description


Specifies a 3x2 matrix that describes a transform. 


## -struct-fields




### -field S_11

The value at the (1,1) position of the matrix (first row, first column).


### -field S_12

The value at the (1,2) position of the matrix (first row, second column).


### -field S_21

The value at the (2,1) position of the matrix (second row, first column).


### -field S_22

The value at the (2,2) position of the matrix (second row, second column).


### -field DX

The value at the (3,1) position of the matrix (third row, first column).


### -field DY

The value at the (3,2) position of the matrix (third row, second column).


## -remarks



In Windows Vista, this structure was named MIL_MATRIX3X2D. It was renamed in Windows 7.



