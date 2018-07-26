---
UID: NS:dwrite_3.DWRITE_COLOR_GLYPH_RUN1
title: DWRITE_COLOR_GLYPH_RUN1
author: windows-sdk-content
description: Represents a color glyph run. The IDWriteFactory4::TranslateColorGlyphRun method returns an ordered collection of color glyph runs of varying types depending on what the font supports.
old-location: directwrite\dwrite_color_glyph_run1.htm
old-project: DirectWrite
ms.assetid: 4433AFDF-F034-43DF-A030-4D7DD6E9CFF5
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: DWRITE_COLOR_GLYPH_RUN1, DWRITE_COLOR_GLYPH_RUN1 structure [Direct Write], directwrite.dwrite_color_glyph_run1, dwrite_3/DWRITE_COLOR_GLYPH_RUN1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_COLOR_GLYPH_RUN1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_COLOR_GLYPH_RUN1 structure


## -description


Represents a color glyph run. The IDWriteFactory4::TranslateColorGlyphRun method returns an ordered collection of color glyph runs of varying types depending on what the font supports.


## -struct-fields




### -field glyphImageFormat

Type of glyph image format for this color run. Exactly one type will be set since TranslateColorGlyphRun has already broken down the run into separate parts.


### -field measuringMode

Measuring mode to use for this glyph run.


### -field DWRITE_COLOR_GLYPH_RUN

 



