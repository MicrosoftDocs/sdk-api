---
UID: NS:d2d1.D2D1_BRUSH_PROPERTIES
title: D2D1_BRUSH_PROPERTIES
author: windows-sdk-content
description: Describes the opacity and transformation of a brush.
old-location: direct2d\D2D1_BRUSH_PROPERTIES.htm
tech.root: direct2d
ms.assetid: 37b2fc18-a320-41c0-8717-dcd561a2f2df
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: D2D1_BRUSH_PROPERTIES, D2D1_BRUSH_PROPERTIES structure [Direct2D], d2d1/D2D1_BRUSH_PROPERTIES, direct2d.D2D1_BRUSH_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_BRUSH_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_BRUSH_PROPERTIES
req.redist: 
---

# D2D1_BRUSH_PROPERTIES structure


## -description


Describes the opacity and transformation of a brush.


## -struct-fields




### -field opacity

Type: <b>FLOAT</b>

A value between 0.0f and 1.0f, inclusive, that specifies the degree of opacity of the brush.


### -field transform

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_3X2_F</a></b>

The transformation that is applied to the brush.


## -remarks



This structure is used when creating a brush. For convenience, Direct2D provides the <a href="https://msdn.microsoft.com/en-us/library/Dd370904(v=VS.85).aspx">D2D1::BrushProperties</a> function for creating <b>D2D1_BRUSH_PROPERTIES</b> structures.

After creating a brush, you can change its opacity or transform by calling the <a href="https://msdn.microsoft.com/c2e6df27-4007-4f2e-9567-439dd3842318">SetOpacity</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd742690(v=VS.85).aspx">SetTransform</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd370904(v=VS.85).aspx">D2D1::BrushProperties</a>



<a href="https://msdn.microsoft.com/c2e6df27-4007-4f2e-9567-439dd3842318">SetOpacity</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742690(v=VS.85).aspx">SetTransform</a>
 

 

