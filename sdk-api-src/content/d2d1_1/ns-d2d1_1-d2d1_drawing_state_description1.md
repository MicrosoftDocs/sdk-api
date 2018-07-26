---
UID: NS:d2d1_1.D2D1_DRAWING_STATE_DESCRIPTION1
title: D2D1_DRAWING_STATE_DESCRIPTION1
author: windows-sdk-content
description: Describes the drawing state of a device context.
old-location: direct2d\d2d1_drawing_state_description1.htm
old-project: Direct2D
ms.assetid: E1BFF353-8445-435C-8F7A-E93BFE58A794
ms.author: windowssdkdev
ms.date: 07/23/2018
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
req.type-library: D2D1.lib
tech.root: 
req.typenames: D2D1_DRAWING_STATE_DESCRIPTION1
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
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_DRAWING_STATE_DESCRIPTION1 structure


## -description


Describes the drawing state of a device context.


## -struct-fields




### -field antialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent nontext drawing operations. 


### -field textAntialiasMode

Type: <b><a href="https://msdn.microsoft.com/d2c829d7-9892-4cbb-9993-12bb7d77fc25">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent text and glyph drawing operations.


### -field tag1

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a></b>

A label for subsequent drawing operations.


### -field tag2

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a></b>

A label for subsequent drawing operations.


### -field transform

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to subsequent drawing operations.


### -field primitiveBlend

Type: <b><a href="https://msdn.microsoft.com/411a42c9-f8d7-46f3-a6e6-51afc83375ad">D2D1_PRIMITIVE_BLEND</a></b>

The blend mode for the device context to apply to subsequent drawing operations.


### -field unitMode

Type: <b><a href="https://msdn.microsoft.com/1ba11761-f3e9-4996-8494-384db5bddc99">D2D1_UNIT_MODE</a></b>

D2D1_UNIT_MODE


## -see-also




<a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a>



<a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a>
 

 

