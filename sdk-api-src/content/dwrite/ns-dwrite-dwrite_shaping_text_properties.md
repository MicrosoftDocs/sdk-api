---
UID: NS:dwrite.DWRITE_SHAPING_TEXT_PROPERTIES
title: DWRITE_SHAPING_TEXT_PROPERTIES (dwrite.h)
description: Shaping output properties for an output glyph.
helpviewer_keywords: ["DWRITE_SHAPING_TEXT_PROPERTIES","DWRITE_SHAPING_TEXT_PROPERTIES structure [Direct Write]","directwrite.dwrite_shaping_text_properties","dwrite/DWRITE_SHAPING_TEXT_PROPERTIES"]
old-location: directwrite\dwrite_shaping_text_properties.htm
tech.root: DirectWrite
ms.assetid: 2fd1af73-c2ea-4077-9cf5-77ab9f237f0a
ms.date: 12/05/2018
ms.keywords: DWRITE_SHAPING_TEXT_PROPERTIES, DWRITE_SHAPING_TEXT_PROPERTIES structure [Direct Write], directwrite.dwrite_shaping_text_properties, dwrite/DWRITE_SHAPING_TEXT_PROPERTIES
req.header: dwrite.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_SHAPING_TEXT_PROPERTIES
 - dwrite/DWRITE_SHAPING_TEXT_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_SHAPING_TEXT_PROPERTIES
---

## -description

Shaping output properties per input character.

## -struct-fields

### -field isShapedAlone

Type: <b>UINT16</b>

Indicates that the character is shaped independently from the others (usually set for the space character).

### -field reserved1

Reserved for use by shaping engine.

### -field canBreakShapingAfter

Glyph shaping can be safely cut after this point without affecting shaping before or after it. Otherwise, splitting a call to [GetGlyphs](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) would cause a reflow of glyph advances and shapes.

### -field reserved

Reserved for use by the shaping engine.

Type: <b>UINT16</b>

Reserved for future use.
