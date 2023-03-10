---
UID: NS:dwrite.DWRITE_SHAPING_GLYPH_PROPERTIES
title: DWRITE_SHAPING_GLYPH_PROPERTIES (dwrite.h)
description: Contains shaping output properties for an output glyph.
helpviewer_keywords: ["DWRITE_SHAPING_GLYPH_PROPERTIES","DWRITE_SHAPING_GLYPH_PROPERTIES structure [Direct Write]","directwrite.dwrite_shaping_glyph_properties","dwrite/DWRITE_SHAPING_GLYPH_PROPERTIES"]
old-location: directwrite\dwrite_shaping_glyph_properties.htm
tech.root: DirectWrite
ms.assetid: debaa84f-8883-4117-9be0-962857b55020
ms.date: 12/05/2018
ms.keywords: DWRITE_SHAPING_GLYPH_PROPERTIES, DWRITE_SHAPING_GLYPH_PROPERTIES structure [Direct Write], directwrite.dwrite_shaping_glyph_properties, dwrite/DWRITE_SHAPING_GLYPH_PROPERTIES
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
 - DWRITE_SHAPING_GLYPH_PROPERTIES
 - dwrite/DWRITE_SHAPING_GLYPH_PROPERTIES
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
 - DWRITE_SHAPING_GLYPH_PROPERTIES
---

# DWRITE_SHAPING_GLYPH_PROPERTIES structure


## -description

Contains shaping output properties for an output glyph.

## -struct-fields

### -field justification

Type: <b>UINT16</b>

Indicates that the glyph has justification applied.

### -field isClusterStart

Type: <b>UINT16</b>

Indicates that the glyph is the start of a cluster.

### -field isDiacritic

Type: <b>UINT16</b>

Indicates that the glyph is a diacritic mark.

### -field isZeroWidthSpace

Type: <b>UINT16</b>

Indicates that the glyph is a word boundary with no visible space.

### -field reserved

Type: <b>UINT16</b>

Reserved for future use.

