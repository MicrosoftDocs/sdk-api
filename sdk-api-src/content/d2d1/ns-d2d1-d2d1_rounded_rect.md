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

# D2D1_ROUNDED_RECT structure


## -description



    Contains the dimensions and corner radii of a rounded rectangle.


## -struct-fields




### -field rect

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The coordinates of the rectangle.


### -field radiusX

Type: <b>FLOAT</b>

The x-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.


### -field radiusY

Type: <b>FLOAT</b>

The y-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.


## -remarks



Each corner of the rectangle specified by the <i>rect</i> is replaced with a quarter ellipse, with a radius in each direction specified by <i>radiusX</i> and <i>radiusY</i>.

 If the <i>radiusX</i> is greater than or equal to half the width of the rectangle, and the <i>radiusY</i> is greater than or equal to one-half the height, the rounded rectangle is an ellipse with the same width and height of the <i>rect</i>. 

Even when both <i>radiuX</i> and <i>radiusY</i> are zero, the rounded rectangle is different from a rectangle., When stroked, the corners of the rounded rectangle are roundly joined, not mitered (square). 



