---
UID: NS:dwrite_3.DWRITE_FONT_PROPERTY
title: DWRITE_FONT_PROPERTY (dwrite_3.h)
description: Font property used for filtering font sets and building a font set with explicit properties.
helpviewer_keywords: ["DWRITE_FONT_PROPERTY","DWRITE_FONT_PROPERTY structure [Direct Write]","directwrite.dwrite_font_property","dwrite_3/DWRITE_FONT_PROPERTY"]
old-location: directwrite\dwrite_font_property.htm
tech.root: DirectWrite
ms.assetid: C169B175-74FD-423A-8E0A-DC50314D75E6
ms.date: 09/10/2025
ms.keywords: DWRITE_FONT_PROPERTY, DWRITE_FONT_PROPERTY structure [Direct Write], directwrite.dwrite_font_property, dwrite_3/DWRITE_FONT_PROPERTY
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - DWRITE_FONT_PROPERTY
 - dwrite_3/DWRITE_FONT_PROPERTY
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
 - DWRITE_FONT_PROPERTY
---

# DWRITE_FONT_PROPERTY structure


## -description

Font property used for filtering font sets and
      building a font set with explicit properties.

## -struct-fields

### -field propertyId

Specifies the requested font property, such as DWRITE_FONT_PROPERTY_ID_FAMILY_NAME.

### -field propertyValue

Specifies the value, such as "Segoe UI".

### -field localeName

Specifies the locale to use, such as "en-US". Simply leave this empty when used
          with the font set filtering functions, as they will find a match regardless of
          language. For passing to AddFontFaceReference, the localeName specifies the language
          of the property value.

