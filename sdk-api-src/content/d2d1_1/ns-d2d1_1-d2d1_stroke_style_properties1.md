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

# D2D1_STROKE_STYLE_PROPERTIES1 structure


## -description


Describes the stroke that outlines a shape.


## -struct-fields




### -field startCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The cap to use at the start of each open figure.


### -field endCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The cap to use at the end of each open figure.


### -field dashCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The cap to use at the start and end of each dash.


### -field lineJoin

Type: <b><a href="https://msdn.microsoft.com/4368e93e-af69-4555-ac2b-c9c576c81372">D2D1_LINE_JOIN</a></b>

The line join to use.


### -field miterLimit

Type: <b>FLOAT</b>

The limit beyond which miters are either clamped or converted to bevels.


### -field dashStyle

Type: <b><a href="https://msdn.microsoft.com/0c1807e3-51e6-440a-bd80-9b43ed7a39f5">D2D1_DASH_STYLE</a></b>

The type of dash to use.


### -field dashOffset

Type: <b>FLOAT</b>

The location of the first dash, relative to the start of the figure. 


### -field transformType

Type: <b><a href="https://msdn.microsoft.com/99c2c5c8-49ce-4865-befa-e9f92905a260">D2D1_STROKE_TRANSFORM_TYPE</a></b>

The rule that determines what render target properties affect the nib of the stroke.


## -see-also




<a href="https://msdn.microsoft.com/1812cd62-e2d7-4f56-ac72-4b0a2b77fd14">ID2D1Factory1::CreateStrokeStyle</a>



<a href="https://msdn.microsoft.com/7afaa6f8-8e25-42ec-9afb-a5342bba11d0">ID2D1StrokeStyle1</a>
 

 

