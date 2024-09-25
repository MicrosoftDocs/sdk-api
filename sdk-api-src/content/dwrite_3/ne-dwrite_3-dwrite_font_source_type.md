---
UID: NE:dwrite_3.DWRITE_FONT_SOURCE_TYPE
title: DWRITE_FONT_SOURCE_TYPE
description: Defines constants that specify the mechanism by which a font came to be included in a font set.
helpviewer_keywords: ["DWRITE_FONT_SOURCE_TYPE","DWRITE_FONT_SOURCE_TYPE enumeration [Direct Write]","directwrite.dwrite_font_source_type","dwrite_3/DWRITE_FONT_SOURCE_TYPE"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: DWRITE_FONT_SOURCE_TYPE, DWRITE_FONT_SOURCE_TYPE enumeration [Direct Write], directwrite.dwrite_font_source_type, dwrite_3/DWRITE_FONT_SOURCE_TYPE
req.construct-type: enumeration
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 17763
req.target-min-winversvr: Windows 10 Build 17763
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
f1_keywords:
 - DWRITE_FONT_SOURCE_TYPE
 - dwrite_3/DWRITE_FONT_SOURCE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_FONT_SOURCE_TYPE
---

## -description

Defines constants that specify the mechanism by which a font came to be included in a font set.

## -enum-fields

### -field DWRITE_FONT_SOURCE_TYPE_UNKNOWN

Specifies that the font source is unknown, or is not any of the other defined font source types.

### -field DWRITE_FONT_SOURCE_TYPE_PER_MACHINE

Specifies that the font source is a font file that's installed for all users on the device.

### -field DWRITE_FONT_SOURCE_TYPE_PER_USER

Specifies that the font source is a font file that's installed for the current user.

### -field DWRITE_FONT_SOURCE_TYPE_APPX_PACKAGE

Specifies that the font source is an APPX package, which includes one or more font files. The font source name is the full name of the package.

### -field DWRITE_FONT_SOURCE_TYPE_REMOTE_FONT_PROVIDER

Specifies that the font source is a font provider for downloadable fonts.

## -remarks

## -see-also

