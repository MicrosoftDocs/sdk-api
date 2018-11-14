---
UID: NF:d2d1helper.BrushProperties
title: BrushProperties function
author: windows-sdk-content
description: Creates a D2D1_BRUSH_PROPERTIES structure.
old-location: direct2d\brushproperties.htm
tech.root: direct2d
ms.assetid: eeb438e4-300a-4d7d-b8bf-91baba4a729e
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: BrushProperties, BrushProperties function [Direct2D], d2d1helper/BrushProperties, direct2d.brushproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - BrushProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BrushProperties
: 
---

# BrushProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a> structure.


## -parameters




### -param opacity [in]

Type: <b>FLOAT</b>

The base opacity of the brush. The default value is 1.0.


### -param transform [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to the brush. The default value is <a href="https://msdn.microsoft.com/09c2ed59-db4a-4753-a98a-bef7748d3803">D2D1::IdentityMatrix</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a></b>

The new brush properties structure. 




## -see-also




<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>
 

 

