---
UID: NS:d2d1_1.D2D1_DRAWING_STATE_DESCRIPTION1
title: D2D1_DRAWING_STATE_DESCRIPTION1
author: windows-sdk-content
description: Describes the drawing state of a device context.
old-location: direct2d\d2d1_drawing_state_description1.htm
tech.root: direct2d
ms.assetid: E1BFF353-8445-435C-8F7A-E93BFE58A794
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: D2D1_DRAWING_STATE_DESCRIPTION1, D2D1_DRAWING_STATE_DESCRIPTION1 structure [Direct2D], d2d1_1/D2D1_DRAWING_STATE_DESCRIPTION1, direct2d.d2d1_drawing_state_description1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_1.h
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
 - D2D1_1.h
api_name:
 - D2D1_DRAWING_STATE_DESCRIPTION1
product: Windows
targetos: Windows
req.typenames: D2D1_DRAWING_STATE_DESCRIPTION1
req.redist: 
---

# D2D1_DRAWING_STATE_DESCRIPTION1 structure


## -description


Describes the drawing state of a device context.


## -struct-fields




### -field antialiasMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368061(v=VS.85).aspx">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent nontext drawing operations. 


### -field textAntialiasMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368170(v=VS.85).aspx">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent text and glyph drawing operations.


### -field tag1

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368168(v=VS.85).aspx">D2D1_TAG</a></b>

A label for subsequent drawing operations.


### -field tag2

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368168(v=VS.85).aspx">D2D1_TAG</a></b>

A label for subsequent drawing operations.


### -field transform

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to subsequent drawing operations.


### -field primitiveBlend

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh447008(v=VS.85).aspx">D2D1_PRIMITIVE_BLEND</a></b>

The blend mode for the device context to apply to subsequent drawing operations.


### -field unitMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh447022(v=VS.85).aspx">D2D1_UNIT_MODE</a></b>

D2D1_UNIT_MODE


## -see-also




<a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a>



<a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a>
 

 

