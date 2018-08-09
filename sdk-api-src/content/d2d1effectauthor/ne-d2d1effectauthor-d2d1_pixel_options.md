---
UID: NE:d2d1effectauthor.D2D1_PIXEL_OPTIONS
title: D2D1_PIXEL_OPTIONS
author: windows-sdk-content
description: Indicates how pixel shader sampling will be restricted.
old-location: direct2d\d2d1_pixel_options.htm
old-project: direct2d
ms.assetid: 285cf526-d8f6-4ae7-a017-066e397078b0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_PIXEL_OPTIONS, D2D1_PIXEL_OPTIONS enumeration [Direct2D], D2D1_PIXEL_OPTIONS_NONE, D2D1_PIXEL_OPTIONS_TRIVIAL_SAMPLING, d2d1effectauthor/D2D1_PIXEL_OPTIONS, d2d1effectauthor/D2D1_PIXEL_OPTIONS_NONE, d2d1effectauthor/D2D1_PIXEL_OPTIONS_TRIVIAL_SAMPLING, direct2d.d2d1_pixel_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
tech.root: 
req.typenames: D2D1_PIXEL_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_PIXEL_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

