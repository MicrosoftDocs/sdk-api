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

# Matrix3x2F::Skew


## -description


Creates a skew transformation that has the specified x-axis and y-axis values and center point.


## -parameters




### -param angleX

Type: <b>FLOAT</b>

The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.


### -param angleY

Type: <b>FLOAT</b>

The y-axis skew angle, which is measured in degrees clockwise from the x-axis.


### -param center






#### - centerPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point about which the skew is performed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

The new skew transformation.




## -remarks



The typical y-axis skew means skews the angle in degrees counterclockwise from the x-axis. However, because the y-axis in Direct2D is inverted, the y-axis skew angle in Direct2D means skew the angle in degrees clockwise from the x-axis.

For example, the following illustration shows the rectangle skewed with y-axis skew angle of 30 degrees.  Notice that the angle is 30 degrees clockwise from the x-axis. 

<img alt="Illustration of a rectangle that is skewed along the y-axis for 30 degrees" src="images/skewy.png"/>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff">How to Skew an Object</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

