---
UID: NF:gdipluspixelformats.IsIndexedPixelFormat
title: IsIndexedPixelFormat function (gdipluspixelformats.h)
description: The IsIndexedPixelFormat method determines whether a specified pixel format is an indexed format.helpviewer_keywords: ["IsIndexedPixelFormat","IsIndexedPixelFormat function [GDI+]","_gdiplus_FUNC_IsIndexedPixelFormat_","gdiplus._gdiplus_FUNC_IsIndexedPixelFormat_","gdipluspixelformats/IsIndexedPixelFormat"]
old-location: gdiplus\_gdiplus_FUNC_IsIndexedPixelFormat_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\isindexedpixelformat.htm
ms.date: 12/05/2018
ms.keywords: IsIndexedPixelFormat, IsIndexedPixelFormat function [GDI+], _gdiplus_FUNC_IsIndexedPixelFormat_, gdiplus._gdiplus_FUNC_IsIndexedPixelFormat_, gdipluspixelformats/IsIndexedPixelFormat
f1_keywords:
- gdipluspixelformats/IsIndexedPixelFormat
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- Gdiplus.lib
- Gdiplus.dll
api_name:
- IsIndexedPixelFormat
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# IsIndexedPixelFormat function


## -description


The <b>IsIndexedPixelFormat</b> method determines whether a specified pixel format is an indexed format.


## -parameters




### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat</a> constant that specifies the pixel format to be tested.


## -returns



Type: <b>BOOL</b>

If the pixel format is an indexed format, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.



