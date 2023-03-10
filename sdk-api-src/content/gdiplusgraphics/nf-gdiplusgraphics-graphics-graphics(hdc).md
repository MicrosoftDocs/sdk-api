---
UID: NF:gdiplusgraphics.Graphics.Graphics(HDC)
title: Graphics::Graphics
description: Creates a Graphics::Graphics object that is associated with a specified device context.
tech.root: gdiplus
helpviewer_keywords: ["Graphics::Graphics"]
ms.assetid: f048c2f7-27b4-48dc-b6d8-871f010603f5
ms.date: 05/13/2019
ms.keywords: Graphics::Graphics
targetos: Windows
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
f1_keywords:
 - Graphics::Graphics
 - gdiplusgraphics/Graphics::Graphics
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::Graphics
---

# Graphics(HDC)


## -description

Creates a **Graphics::Graphics** object that is associated with a specified device context.

## -parameters

### -param hdc

Handle to a device context that will be associated with the new **Graphics::Graphics** object.

## -remarks

When you use this constructor to create a **Graphics::Graphics** object, make sure that the **Graphics::Graphics** object is deleted or goes out of scope before the device context is released.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>

<a href="/windows/desktop/gdiplus/-gdiplus-getting-started-use">Getting Started</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>