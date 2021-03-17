---
UID: NS:dwrite.DWRITE_TYPOGRAPHIC_FEATURES
title: DWRITE_TYPOGRAPHIC_FEATURES (dwrite.h)
description: Contains a set of typographic features to be applied during text shaping.
helpviewer_keywords: ["DWRITE_TYPOGRAPHIC_FEATURES","DWRITE_TYPOGRAPHIC_FEATURES structure [Direct Write]","directwrite.dwrite_typographic_features","dwrite/DWRITE_TYPOGRAPHIC_FEATURES"]
old-location: directwrite\dwrite_typographic_features.htm
tech.root: DirectWrite
ms.assetid: 21ef4266-5dd6-48b6-9175-452b74e94a07
ms.date: 12/05/2018
ms.keywords: DWRITE_TYPOGRAPHIC_FEATURES, DWRITE_TYPOGRAPHIC_FEATURES structure [Direct Write], directwrite.dwrite_typographic_features, dwrite/DWRITE_TYPOGRAPHIC_FEATURES
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
 - DWRITE_TYPOGRAPHIC_FEATURES
 - dwrite/DWRITE_TYPOGRAPHIC_FEATURES
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
 - DWRITE_TYPOGRAPHIC_FEATURES
---

# DWRITE_TYPOGRAPHIC_FEATURES structure


## -description

Contains a set of typographic features to be applied during text shaping.

## -struct-fields

### -field features

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature">DWRITE_FONT_FEATURE</a>*</b>

A pointer to a structure that specifies properties used to identify and execute typographic features in the font.

### -field featureCount

Type: <b>UINT32</b>

A value that indicates the number of features being applied to a font face.

