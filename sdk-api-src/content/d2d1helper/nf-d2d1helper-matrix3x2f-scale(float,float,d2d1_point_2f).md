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

# Matrix3x2F::Scale(FLOAT,FLOAT,D2D1_POINT_2F)


## -description


Creates a scale transformation that has the specified scale factors and center point. 


## -parameters




### -param x

Type: <b>FLOAT</b>

The x-axis scale factor of the scale transformation.


### -param y

Type: <b>FLOAT</b>

The y-axis scale factor of the scale transformation.


### -param center






#### - centerPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point about which the scale is performed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

The new scale transformation.




## -remarks



This method creates a scale transformation for the specified <i>centerPoint</i> and the 
	 x-axis and y-axis scale factors. If you prefer to create a  
	 <a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a> structure to store the scale factors, call the other <a href="https://msdn.microsoft.com/c2aa64eb-c69a-4938-91de-1541f1c7844f">Scale</a> method. 

The following illustration shows the size of the square increased 
	 to 130% in both dimensions.
	 The center point of the scaling is the upper-left corner of the square.

<img alt="Illustration of a square scaled by 130% in the x-direction and y-direction" src="images/scale_ovw.png"/>

 For an example, see <a href="https://msdn.microsoft.com/3da749e2-50d5-4f4e-9ccd-8c230efe3436">How to Scale an Object</a>.




## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

