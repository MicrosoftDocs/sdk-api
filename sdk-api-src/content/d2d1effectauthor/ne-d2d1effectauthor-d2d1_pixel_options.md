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

# D2D1_PIXEL_OPTIONS enumeration


## -description


Indicates how pixel shader sampling will be restricted. This indicates whether the vertex buffer is large and tends to change infrequently or smaller and changes frequently (typically frame over frame).

    
  
   
 
  
  


## -enum-fields




### -field D2D1_PIXEL_OPTIONS_NONE

The pixel shader is not restricted in its sampling.


### -field D2D1_PIXEL_OPTIONS_TRIVIAL_SAMPLING

 The pixel shader samples inputs only at the same scene coordinate as the output pixel and returns transparent black whenever the input pixels are also transparent black.


### -field D2D1_PIXEL_OPTIONS_FORCE_DWORD




## -remarks





If the shader specifies <b>D2D1_PIXEL_OPTIONS_NONE</b>, it must still correctly implement the region of interest calculations in <a href="https://msdn.microsoft.com/EE098F67-B5A7-41C1-886A-2C7779B5E05C">ID2D1Transform::MapOutputRectToInputRects</a> and <a href="https://msdn.microsoft.com/8FC15A61-767C-460A-A260-9F56A41DA87F">ID2D1Transform::MapInputRectsToOutputRect</a>.




## -see-also




<a href="https://msdn.microsoft.com/9CB38592-6B49-48FE-AA3F-1FC402489454">ID2D1DrawInfo::SetPixelShader</a>
 

 

