---
UID: NS:dwrite.DWRITE_FONT_FEATURE
title: DWRITE_FONT_FEATURE (dwrite.h)
description: Specifies properties used to identify and execute typographic features in the current font face.
helpviewer_keywords: ["DWRITE_FONT_FEATURE","DWRITE_FONT_FEATURE structure [Direct Write]","directwrite.dwrite_font_feature","dwrite/DWRITE_FONT_FEATURE"]
old-location: directwrite\dwrite_font_feature.htm
tech.root: DirectWrite
ms.assetid: f8c2b1b0-ecab-4556-b3e6-5eda75e206ed
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_FEATURE, DWRITE_FONT_FEATURE structure [Direct Write], directwrite.dwrite_font_feature, dwrite/DWRITE_FONT_FEATURE
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
 - DWRITE_FONT_FEATURE
 - dwrite/DWRITE_FONT_FEATURE
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
 - DWRITE_FONT_FEATURE
---

# DWRITE_FONT_FEATURE structure


## -description

Specifies properties used to identify and execute typographic features in the current font face.

## -struct-fields

### -field nameTag

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag">DWRITE_FONT_FEATURE_TAG</a></b>

The feature OpenType name identifier.

### -field parameter

Type: <b>UINT32</b>

The execution parameter of the feature.

## -remarks

A non-zero value generally enables the feature execution, while the zero value disables it. A feature requiring a selector uses this value to indicate the selector index.

The OpenType standard provides access to typographic features available in the font by means of a feature tag with the associated parameters. The OpenType feature tag is a 4-byte identifier of the registered name of a feature. For example, the 'kern' feature name tag is used to identify the 'Kerning' feature in OpenType font. Similarly, the OpenType feature tag for 'Standard Ligatures' and 'Fractions' is 'liga' and 'frac' respectively. Since a single run can be associated with more than one typographic features, the Text String API accepts typographic settings for a run as a list of features and are executed in the order they are specified.

The value of the tag member represents the OpenType name tag of the feature, while the param value represents additional parameter for the execution of the feature referred by the tag member. Both <b>nameTag</b> and <b>parameter</b> are stored as little endian, the same convention followed by GDI.  Most features treat the Param value as a binary value that indicates whether to turn the execution of the feature on or off, with it being off by default in the majority of cases. Some features, however, treat this value as an integral value representing the integer index to the list of alternate results it may produce during the execution; for instance, the feature 'Stylistic Alternates' or 'salt' uses the <b>parameter</b> value as an index to the list of alternate substituting glyphs it could produce for a specified glyph.

