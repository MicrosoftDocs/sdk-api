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

# IXpsOMGradientBrush::SetColorInterpolationMode


## -description


Sets the <a href="https://msdn.microsoft.com/ad203082-d5a3-4414-88e1-8fd4dded6ea9">XPS_COLOR_INTERPOLATION</a> value, which describes the gamma function to be used for color interpolation.


## -parameters




### -param colorInterpolationMode [in]

The <a href="https://msdn.microsoft.com/ad203082-d5a3-4414-88e1-8fd4dded6ea9">XPS_COLOR_INTERPOLATION</a> value, which describes the gamma function to be used for color interpolation.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/ad203082-d5a3-4414-88e1-8fd4dded6ea9">XPS_COLOR_INTERPOLATION</a>
 

 

