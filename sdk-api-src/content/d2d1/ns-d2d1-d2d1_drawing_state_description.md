---
UID: NS:d2d1.D2D1_DRAWING_STATE_DESCRIPTION
title: D2D1_DRAWING_STATE_DESCRIPTION
author: windows-sdk-content
description: Describes the drawing state of a render target.
old-location: direct2d\D2D1_DRAWING_STATE_DESCRIPTION.htm
old-project: direct2d
ms.assetid: ba4adc4b-4d86-40c4-8911-1c800d3c6f3e
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: D2D1_DRAWING_STATE_DESCRIPTION, D2D1_DRAWING_STATE_DESCRIPTION structure [Direct2D], d2d1/D2D1_DRAWING_STATE_DESCRIPTION, direct2d.D2D1_DRAWING_STATE_DESCRIPTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_DRAWING_STATE_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_DRAWING_STATE_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_DRAWING_STATE_DESCRIPTION structure


## -description


Describes the drawing state of a render target.  


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


## -see-also




<a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a>



<a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a>
 

 

