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

# InkStyleProperties function


## -description



          Creates a <a href="https://msdn.microsoft.com/81B9E108-D0A6-4F7E-8BE9-76A570B1D050">D2D1_INK_STYLE_PROPERTIES</a> structure.
        


## -parameters




### -param nibShape

Type: <b><a href="https://msdn.microsoft.com/E9EA4F3E-D539-4938-897F-467D0432174F">D2D1_INK_NIB_SHAPE</a></b>

The pre-transform shape of the nib (pen tip) used to draw a given ink object.


### -param nibTransform [ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transform applied to the nib. Note that the translation components of the transform matrix are ignored for the purposes of rendering.


## -returns



Type: <b><a href="https://msdn.microsoft.com/81B9E108-D0A6-4F7E-8BE9-76A570B1D050">D2D1_INK_STYLE_PROPERTIES</a></b>


            Returns the created <a href="https://msdn.microsoft.com/81B9E108-D0A6-4F7E-8BE9-76A570B1D050">D2D1_INK_STYLE_PROPERTIES</a> structure.
          




## -see-also




<a href="https://msdn.microsoft.com/81B9E108-D0A6-4F7E-8BE9-76A570B1D050">D2D1_INK_STYLE_PROPERTIES</a>
 

 

