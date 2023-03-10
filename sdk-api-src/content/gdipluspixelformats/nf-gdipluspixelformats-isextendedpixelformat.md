---
UID: NF:gdipluspixelformats.IsExtendedPixelFormat
title: IsExtendedPixelFormat function (gdipluspixelformats.h)
description: The IsExtendedPixelFormat method determines whether a specified pixel format uses 16 bits per color channel.
helpviewer_keywords: ["IsExtendedPixelFormat","IsExtendedPixelFormat function [GDI+]","_gdiplus_FUNC_IsExtendedPixelFormat_","gdiplus._gdiplus_FUNC_IsExtendedPixelFormat_","gdipluspixelformats/IsExtendedPixelFormat"]
old-location: gdiplus\_gdiplus_FUNC_IsExtendedPixelFormat_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\isextendedpixelformat.htm
ms.date: 12/05/2018
ms.keywords: IsExtendedPixelFormat, IsExtendedPixelFormat function [GDI+], _gdiplus_FUNC_IsExtendedPixelFormat_, gdiplus._gdiplus_FUNC_IsExtendedPixelFormat_, gdipluspixelformats/IsExtendedPixelFormat
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
 - IsExtendedPixelFormat
 - gdipluspixelformats/IsExtendedPixelFormat
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
 - IsExtendedPixelFormat
---

# IsExtendedPixelFormat function


## -description

The <b>IsExtendedPixelFormat</b> method determines whether a specified pixel format uses 16 bits per color channel.

## -parameters

### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat</a> constant that specifies the pixel format to be tested.

## -returns

Type: <b>BOOL</b>

If the pixel format uses 16 bits per color channel, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.