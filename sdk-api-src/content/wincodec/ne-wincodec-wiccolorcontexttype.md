---
UID: NE:wincodec.WICColorContextType
title: WICColorContextType (wincodec.h)
description: Specifies the color context types.
helpviewer_keywords: ["WICColorContextExifColorSpace","WICColorContextProfile","WICColorContextType","WICColorContextType enumeration [Windows Imaging Component]","WICColorContextUninitialized","_wic_codec_wiccolorcontexttype","wic._wic_codec_wiccolorcontexttype","wincodec/WICColorContextExifColorSpace","wincodec/WICColorContextProfile","wincodec/WICColorContextType","wincodec/WICColorContextUninitialized"]
old-location: wic\_wic_codec_wiccolorcontexttype.htm
tech.root: wic
ms.assetid: 30fab53b-8edf-488c-a6f2-5224b94e0500
ms.date: 12/05/2018
ms.keywords: WICColorContextExifColorSpace, WICColorContextProfile, WICColorContextType, WICColorContextType enumeration [Windows Imaging Component], WICColorContextUninitialized, _wic_codec_wiccolorcontexttype, wic._wic_codec_wiccolorcontexttype, wincodec/WICColorContextExifColorSpace, wincodec/WICColorContextProfile, wincodec/WICColorContextType, wincodec/WICColorContextUninitialized
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICColorContextType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICColorContextType
 - wincodec/WICColorContextType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICColorContextType
---

# WICColorContextType enumeration


## -description

Specifies the color context types.

## -enum-fields

### -field WICColorContextUninitialized:0

An uninitialized color context.

### -field WICColorContextProfile:0x1

A color context that is a full ICC color profile.

### -field WICColorContextExifColorSpace:0x2

A color context that is one of a number of set color spaces (sRGB, AdobeRGB) that are defined in the EXIF specification.

