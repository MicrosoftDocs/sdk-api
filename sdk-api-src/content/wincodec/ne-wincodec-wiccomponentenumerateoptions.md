---
UID: NE:wincodec.WICComponentEnumerateOptions
title: WICComponentEnumerateOptions (wincodec.h)
description: Specifies component enumeration options.
helpviewer_keywords: ["WICComponentEnumerateBuiltInOnly","WICComponentEnumerateDefault","WICComponentEnumerateDisabled","WICComponentEnumerateOptions","WICComponentEnumerateOptions enumeration [Windows Imaging Component]","WICComponentEnumerateRefresh","WICComponentEnumerateUnsigned","_wic_codec_wiccomponentenumerateoptions","wic._wic_codec_wiccomponentenumerateoptions","wincodec/WICComponentEnumerateBuiltInOnly","wincodec/WICComponentEnumerateDefault","wincodec/WICComponentEnumerateDisabled","wincodec/WICComponentEnumerateOptions","wincodec/WICComponentEnumerateRefresh","wincodec/WICComponentEnumerateUnsigned"]
old-location: wic\_wic_codec_wiccomponentenumerateoptions.htm
tech.root: wic
ms.assetid: 52cc0860-6164-4400-8e81-03eb0c44904e
ms.date: 12/05/2018
ms.keywords: WICComponentEnumerateBuiltInOnly, WICComponentEnumerateDefault, WICComponentEnumerateDisabled, WICComponentEnumerateOptions, WICComponentEnumerateOptions enumeration [Windows Imaging Component], WICComponentEnumerateRefresh, WICComponentEnumerateUnsigned, _wic_codec_wiccomponentenumerateoptions, wic._wic_codec_wiccomponentenumerateoptions, wincodec/WICComponentEnumerateBuiltInOnly, wincodec/WICComponentEnumerateDefault, wincodec/WICComponentEnumerateDisabled, wincodec/WICComponentEnumerateOptions, wincodec/WICComponentEnumerateRefresh, wincodec/WICComponentEnumerateUnsigned
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WICComponentEnumerateOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICComponentEnumerateOptions
 - wincodec/WICComponentEnumerateOptions
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
 - WICComponentEnumerateOptions
---

# WICComponentEnumerateOptions enumeration


## -description

Specifies component enumeration options.

## -enum-fields

### -field WICComponentEnumerateDefault:0

Enumerate any components that are not disabled. Because this value is 0x0, it is always included with the other options.

### -field WICComponentEnumerateRefresh:0x1

Force a read of the registry before enumerating components.

### -field WICComponentEnumerateDisabled:0x80000000

Include disabled components in the enumeration. The set of disabled components is disjoint with the set of default enumerated components

### -field WICComponentEnumerateUnsigned:0x40000000

Include unsigned components in the enumeration. This option has no effect.

### -field WICComponentEnumerateBuiltInOnly:0x20000000

At the end of component enumeration, filter out any components that are not Windows provided.

### -field WICCOMPONENTENUMERATEOPTIONS_FORCE_DWORD:0x7fffffff

