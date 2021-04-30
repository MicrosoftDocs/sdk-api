---
UID: NF:gdipluspixelformats.IsAlphaPixelFormat
title: IsAlphaPixelFormat function (gdipluspixelformats.h)
description: The IsAlphaPixelFormat method determines whether a specified pixel format has an alpha component.
helpviewer_keywords: ["IsAlphaPixelFormat","IsAlphaPixelFormat function [GDI+]","_gdiplus_FUNC_IsAlphaPixelFormat_","gdiplus._gdiplus_FUNC_IsAlphaPixelFormat_","gdipluspixelformats/IsAlphaPixelFormat"]
old-location: gdiplus\_gdiplus_FUNC_IsAlphaPixelFormat_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\isalphapixelformat.htm
ms.date: 12/05/2018
ms.keywords: IsAlphaPixelFormat, IsAlphaPixelFormat function [GDI+], _gdiplus_FUNC_IsAlphaPixelFormat_, gdiplus._gdiplus_FUNC_IsAlphaPixelFormat_, gdipluspixelformats/IsAlphaPixelFormat
req.header: gdipluspixelformats.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - IsAlphaPixelFormat
 - gdipluspixelformats/IsAlphaPixelFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - IsAlphaPixelFormat
---

# IsAlphaPixelFormat function


## -description

The <b>IsAlphaPixelFormat</b> method determines whether a specified pixel format has an alpha component.

## -parameters

### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat</a> constant that specifies the pixel format to be tested.

## -returns

Type: <b>BOOL</b>

If the pixel format has an alpha component, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.