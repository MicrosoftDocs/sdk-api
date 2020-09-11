---
UID: NE:dwrite.DWRITE_TEXTURE_TYPE
title: DWRITE_TEXTURE_TYPE (dwrite.h)
description: Identifies a type of alpha texture.
helpviewer_keywords: ["DWRITE_TEXTURE_ALIASED_1x1","DWRITE_TEXTURE_CLEARTYPE_3x1","DWRITE_TEXTURE_TYPE","DWRITE_TEXTURE_TYPE enumeration [Direct Write]","directwrite.dwrite_texture_type","dwrite/DWRITE_TEXTURE_ALIASED_1x1","dwrite/DWRITE_TEXTURE_CLEARTYPE_3x1","dwrite/DWRITE_TEXTURE_TYPE"]
old-location: directwrite\dwrite_texture_type.htm
tech.root: DirectWrite
ms.assetid: c97ee0fd-2743-4f72-aa69-bf5e3780aa33
ms.date: 12/05/2018
ms.keywords: DWRITE_TEXTURE_ALIASED_1x1, DWRITE_TEXTURE_CLEARTYPE_3x1, DWRITE_TEXTURE_TYPE, DWRITE_TEXTURE_TYPE enumeration [Direct Write], directwrite.dwrite_texture_type, dwrite/DWRITE_TEXTURE_ALIASED_1x1, dwrite/DWRITE_TEXTURE_CLEARTYPE_3x1, dwrite/DWRITE_TEXTURE_TYPE
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
 - DWRITE_TEXTURE_TYPE
 - dwrite/DWRITE_TEXTURE_TYPE
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
 - DWRITE_TEXTURE_TYPE
---

# DWRITE_TEXTURE_TYPE enumeration


## -description

Identifies a type of alpha texture.

## -enum-fields

### -field DWRITE_TEXTURE_ALIASED_1x1

Specifies an alpha texture for aliased text rendering (that is,  each pixel is either fully opaque or fully transparent), with one byte per pixel.

### -field DWRITE_TEXTURE_CLEARTYPE_3x1

Specifies an alpha texture for ClearType text rendering, with three bytes per pixel in the horizontal dimension and one byte per pixel in the vertical dimension.

## -remarks

An alpha texture is a bitmap of alpha values, each representing opacity of a pixel or subpixel.

