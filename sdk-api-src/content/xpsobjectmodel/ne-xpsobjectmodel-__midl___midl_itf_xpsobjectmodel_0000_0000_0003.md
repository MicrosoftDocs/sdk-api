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

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003 enumeration


## -description


Describes how the spread region is  to be filled. 
 The spread region is the area that falls within the drawing area but outside of the gradient region.


## -enum-fields




### -field XPS_SPREAD_METHOD_PAD

The spread region is filled with the color whose value equals the color  at the end of the gradient region.


### -field XPS_SPREAD_METHOD_REFLECT

The spread region is filled by repeating the alternating reflection of the gradient that is  inside the gradient region.


### -field XPS_SPREAD_METHOD_REPEAT

The spread region is filled by repeating the gradient that is inside the gradient region, in the same orientation and direction.


## -remarks



The following illustration shows the effect of the spread methods on gradients that are drawn by using the <a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a> and <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a> interfaces. The gradient region of an <b>IXpsOMLinearGradientBrush</b> interface is defined by calling the <a href="https://msdn.microsoft.com/f2e40d75-c0de-4cba-850d-0c8c328e2950">SetStartPoint</a> and <a href="https://msdn.microsoft.com/5eec7bda-bbd8-454a-8b32-9db769df91e6">SetEndPoint</a> methods; the gradient region of an  <b>IXpsOMRadialGradientBrush</b> interface is defined by calling the <a href="https://msdn.microsoft.com/7f1fd304-8495-40b3-b11f-7af9924150eb">SetCenter</a>, <a href="https://msdn.microsoft.com/101bebbf-854c-49fa-bc5c-8c81c5d2f7f9">SetGradientOrigin</a>, and <a href="https://msdn.microsoft.com/2d32c0a7-1069-4c76-ba5c-5978e3fd7125">SetRadiiSizes</a>  methods.     The gradient region is the area inside the dashed lines, and the spread area is the area outside of the gradient region.

<img alt="An illustration that shows examples of the spread method" src="../images/XPS_Spread_Method.png"/>



## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

