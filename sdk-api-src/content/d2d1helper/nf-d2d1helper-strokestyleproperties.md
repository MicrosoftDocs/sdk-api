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

# StrokeStyleProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/67f3701f-febd-4afe-803e-c5d9dbcd1b21">D2D1_STROKE_STYLE_PROPERTIES</a> structure. 


## -parameters




### -param startCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The shape at the beginning of a stroke. The default value is <a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE_FLAT</a>.


### -param endCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The shape at the end of a stroke. The default value is <a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE_FLAT</a>.


### -param dashCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The shape  at either end of each dash segment. The default value is <a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE_FLAT</a>. 


### -param lineJoin

Type: <b><a href="https://msdn.microsoft.com/4368e93e-af69-4555-ac2b-c9c576c81372">D2D1_LINE_JOIN</a></b>

A value that describes how segments are joined. The default value is <a href="https://msdn.microsoft.com/4368e93e-af69-4555-ac2b-c9c576c81372">D2D1_LINE_JOIN_MITER</a>.


### -param miterLimit

Type: <b>FLOAT</b>

The limit of the thickness of the join on a mitered corner. This value is always treated as though it is greater than or equal to 1.0f.

The default value is 10.0f.


### -param dashStyle

Type: <b><a href="https://msdn.microsoft.com/0c1807e3-51e6-440a-bd80-9b43ed7a39f5">D2D1_DASH_STYLE</a></b>

A value that specifies whether the stroke has a dash pattern and, if so, the dash style. 

The default value is <a href="https://msdn.microsoft.com/0c1807e3-51e6-440a-bd80-9b43ed7a39f5">D2D1_DASH_STYLE_SOLID</a>.


### -param dashOffset

Type: <b>FLOAT</b>

A value that specifies how far in the dash sequence the stroke will start. 

The default value is 0.0f.


## -returns



Type: <b><a href="https://msdn.microsoft.com/67f3701f-febd-4afe-803e-c5d9dbcd1b21">D2D1_STROKE_STYLE_PROPERTIES</a></b>

The new stroke style.



