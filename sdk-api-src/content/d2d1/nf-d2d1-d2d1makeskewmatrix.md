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

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The center point of the skew operation.


### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains the rotation transformation. You must allocate storate for this parameter.


## -returns



This function does not return a value.



