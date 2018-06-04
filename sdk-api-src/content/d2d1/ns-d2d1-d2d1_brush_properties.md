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

# D2D1_BRUSH_PROPERTIES structure


## -description



    Describes the opacity and transformation of a brush.


## -struct-fields




### -field opacity

Type: <b>FLOAT</b>

A value between 0.0f and 1.0f, inclusive, that specifies the degree of opacity of the brush.


### -field transform

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transformation that is applied to the brush.


## -remarks



This structure is used when creating a brush. For convenience, Direct2D provides the <a href="https://msdn.microsoft.com/eeb438e4-300a-4d7d-b8bf-91baba4a729e">D2D1::BrushProperties</a> function for creating <b>D2D1_BRUSH_PROPERTIES</b> structures.

After creating a brush, you can change its opacity or transform by calling the <a href="https://msdn.microsoft.com/c2e6df27-4007-4f2e-9567-439dd3842318">SetOpacity</a> or <a href="https://msdn.microsoft.com/57afadc1-88c9-4a5b-a83f-63c4c69182a7">SetTransform</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/eeb438e4-300a-4d7d-b8bf-91baba4a729e">D2D1::BrushProperties</a>



<a href="https://msdn.microsoft.com/c2e6df27-4007-4f2e-9567-439dd3842318">SetOpacity</a>



<a href="https://msdn.microsoft.com/57afadc1-88c9-4a5b-a83f-63c4c69182a7">SetTransform</a>
 

 

