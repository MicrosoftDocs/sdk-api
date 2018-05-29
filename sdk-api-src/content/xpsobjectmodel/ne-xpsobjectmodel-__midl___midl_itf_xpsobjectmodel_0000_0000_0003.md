---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003
title: "__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003"
author: windows-sdk-content
description: Describes how the spread region is to be filled.
old-location: xps\xps_spread_method.htm
old-project: printdocs
ms.assetid: 9c9cadaf-6f38-4a56-942e-78617017a905
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: XPS_SPREAD_METHOD, XPS_SPREAD_METHOD enumeration [XPS Documents and Packaging], XPS_SPREAD_METHOD_PAD, XPS_SPREAD_METHOD_REFLECT, XPS_SPREAD_METHOD_REPEAT, __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003, xps.xps_spread_method, xpsobjectmodel/XPS_SPREAD_METHOD, xpsobjectmodel/XPS_SPREAD_METHOD_PAD, xpsobjectmodel/XPS_SPREAD_METHOD_REFLECT, xpsobjectmodel/XPS_SPREAD_METHOD_REPEAT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_SPREAD_METHOD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	xpsobjectmodel.h
api_name:
-	XPS_SPREAD_METHOD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

