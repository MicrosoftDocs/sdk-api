---
UID: NF:gdipluspixelformats.IsCanonicalPixelFormat
title: IsCanonicalPixelFormat function (gdipluspixelformats.h)
description: The IsCanonicalPixelFormat method determines whether a specified pixel format is one of the canonical formats:\_PixelFormat32bppARGB or PixelFormat64bppARGB.
helpviewer_keywords: ["IsCanonicalPixelFormat","IsCanonicalPixelFormat function [GDI+]","_gdiplus_FUNC_IsCanonicalPixelFormat_","gdiplus._gdiplus_FUNC_IsCanonicalPixelFormat_","gdipluspixelformats/IsCanonicalPixelFormat"]
old-location: gdiplus\_gdiplus_FUNC_IsCanonicalPixelFormat_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\iscanonicalpixelformat.htm
ms.date: 12/05/2018
ms.keywords: IsCanonicalPixelFormat, IsCanonicalPixelFormat function [GDI+], _gdiplus_FUNC_IsCanonicalPixelFormat_, gdiplus._gdiplus_FUNC_IsCanonicalPixelFormat_, gdipluspixelformats/IsCanonicalPixelFormat
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
 - IsCanonicalPixelFormat
 - gdipluspixelformats/IsCanonicalPixelFormat
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
 - IsCanonicalPixelFormat
---

# IsCanonicalPixelFormat function


## -description

The <b>IsCanonicalPixelFormat</b> method determines whether a specified pixel format is one of the canonical formats: <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat32bppARGB</a> or <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat64bppARGB</a>.

## -parameters

### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat</a> constant that specifies the pixel format to be tested.

## -returns

Type: <b>BOOL</b>

If the pixel format is <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat32bppARGB</a> or <b>PixelFormat64bppARGB</b>, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.