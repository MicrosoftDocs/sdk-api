---
UID: NF:d2d1_1helper.DrawingStateDescription1
title: DrawingStateDescription1 function
author: windows-sdk-content
description: Creates a D2D1_DRAWING_STATE_DESCRIPTION1 structure.
old-location: direct2d\drawingstatedescription1.htm
tech.root: direct2d
ms.assetid: 9D2F5196-0C37-465E-AFCF-FAAC3C19D3C2
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: DrawingStateDescription1, DrawingStateDescription1 function [Direct2D], d2d1_1helper/DrawingStateDescription1, direct2d.drawingstatedescription1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
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
 - d2d1.dll
api_name:
 - DrawingStateDescription1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DrawingStateDescription1
: 
---

# DrawingStateDescription1 function


## -description


Creates a D2D1_DRAWING_STATE_DESCRIPTION1 structure.


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


### -param primitiveBlend

Type: <b><a href="https://msdn.microsoft.com/411a42c9-f8d7-46f3-a6e6-51afc83375ad">D2D1_PRIMITIVE_BLEND</a></b>

The blend mode of the Direct2D device context.


### -param unitMode

Type: <b><a href="https://msdn.microsoft.com/1ba11761-f3e9-4996-8494-384db5bddc99">D2D1_UNIT_MODE</a></b>

The unit  mode of the drawing operations.  The default is DIPs.


## -returns



Type: <b><a href="https://msdn.microsoft.com/E1BFF353-8445-435C-8F7A-E93BFE58A794">D2D1_DRAWING_STATE_DESCRIPTION1</a></b>

A structure that describes the drawing state of a render target.



