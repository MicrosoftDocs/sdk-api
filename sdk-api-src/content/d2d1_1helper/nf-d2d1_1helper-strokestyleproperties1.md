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

# StrokeStyleProperties1 function


## -description


Returns a filled D2D1_STROKE_STYLE_PROPERTIES1 structure.


## -parameters




### -param startCap

The cap to use at the start of each open figure.


### -param endCap

The cap to use at the end of each open figure.


### -param dashCap

The cap to use at the start and end of each dash.


### -param lineJoin

The line join to use.


### -param miterLimit

The limit beyond which miters are either clamped or converted to bevels.


### -param dashStyle

The type of dash to use.


### -param dashOffset

The location of the first dash, relative to the start of the figure. 


### -param transformType

The rule that determines what render target properties affect the nib of the stroke.


## -returns



Describes the stroke that outlines a shape.



