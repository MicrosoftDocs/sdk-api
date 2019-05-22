---
UID: NF:gdiplusgraphics.Graphics.SetClip
title: Graphics::SetClip
description: The Graphics::SetClip method updates the clipping region of this Graphics object.
ms.assetid: 77ca4449-3bd3-4476-9502-6b05638ecf7f
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::SetClip
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusgraphics.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::SetClip
---

# SetClip(Graphics*,CombineMode)

## -description

The **Graphics::SetClip** method updates the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to a region that is the combination of itself and the clipping region of another **Graphics** object.

## -parameters

### -param g

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that contains the clipping region to be combined with the clipping region of this **Graphics** object.

### -param combineMode

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534092(v=VS.85).aspx">CombineMode</a> enumeration that specifies how the specified region is combined with the clipping region of this **Graphics** object.
The default value is CombineModeReplace.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534092(v=VS.85).aspx">CombineMode</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535792(v=VS.85).aspx">Graphics::IsClipEmpty</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535802(v=VS.85).aspx">Graphics::ResetClip</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535783(v=VS.85).aspx">IntersectClip Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535791(v=VS.85).aspx">TranslateClip Methods</a>
