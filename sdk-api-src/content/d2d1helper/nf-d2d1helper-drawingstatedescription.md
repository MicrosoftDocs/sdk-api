---
UID: NF:d2d1helper.DrawingStateDescription
title: DrawingStateDescription function
author: windows-sdk-content
description: Creates a D2D1_DRAWING_STATE_DESCRIPTION structure.
old-location: direct2d\drawingstatedescription.htm
old-project: direct2d
ms.assetid: a1f81523-bf9b-4807-a095-d2f4081698e3
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: DrawingStateDescription, DrawingStateDescription function [Direct2D], d2d1helper/DrawingStateDescription, direct2d.drawingstatedescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1helper.h
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
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - DrawingStateDescription
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# DrawingStateDescription function


## -description


Creates a <a href="https://msdn.microsoft.com/ba4adc4b-4d86-40c4-8911-1c800d3c6f3e">D2D1_DRAWING_STATE_DESCRIPTION</a> structure.


## -parameters




### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent non-text drawing operations. The default value is  <a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE_PER_PRIMITIVE</a>.


### -param textAntialiasMode

Type: <b><a href="https://msdn.microsoft.com/d2c829d7-9892-4cbb-9993-12bb7d77fc25">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent text and glyph drawing operations. The default value is <a href="https://msdn.microsoft.com/d2c829d7-9892-4cbb-9993-12bb7d77fc25">D2D1_TEXT_ANTIALIAS_MODE_DEFAULT</a>.


### -param tag1

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a></b>

A label for subsequent drawing operations. The default value is 0.


### -param tag2

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a></b>

A label for subsequent drawing operations. The default value is 0.


### -param transform [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transformation to be applied to subsequent drawing operations.  The default value is provided by the <a href="https://msdn.microsoft.com/09c2ed59-db4a-4753-a98a-bef7748d3803"> D2D1::IdentityMatrix</a> function, which returns the identity matrix.


## -returns



Type: <b><a href="https://msdn.microsoft.com/ba4adc4b-4d86-40c4-8911-1c800d3c6f3e">D2D1_DRAWING_STATE_DESCRIPTION</a></b>

A structure that describes the drawing state of a render target.



