---
UID: NF:dwrite.DWRITE_MAKE_OPENTYPE_TAG
title: DWRITE_MAKE_OPENTYPE_TAG macro (dwrite.h)
author: windows-sdk-content
description: Creates an OpenType tag as a 32-bit integer, such that the first character in the tag is the lowest byte (least significant on little endian architectures), which can be used to compare with tags in the font file.
old-location: directwrite\dwrite_make_opentype_tag.htm
tech.root: DirectWrite
ms.assetid: fe93a24a-5f3d-4e73-87ac-b33357c838e3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_MAKE_OPENTYPE_TAG, DWRITE_MAKE_OPENTYPE_TAG macro [Direct Write], directwrite.dwrite_make_opentype_tag, dwrite/DWRITE_MAKE_OPENTYPE_TAG
ms.topic: macro
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_MAKE_OPENTYPE_TAG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DWRITE_MAKE_OPENTYPE_TAG macro


## -description


 Creates an OpenType tag as a 32-bit integer, such that
 the first character in the tag is the lowest byte
 (least significant on little endian architectures),
 which can be used to compare with tags in the font file.
 This macro is compatible with <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_feature_tag">DWRITE_FONT_FEATURE_TAG</a>.


## -parameters




### -param a

Type: <b>char</b>

The first character in the tag.


### -param b

Type: <b>char</b>

The second character in the tag.


### -param c

Type: <b>char</b>

The third character in the tag.


### -param d

Type: <b>char</b>

The fourth character in the tag.


## -remarks



<div class="alert"><b>Note</b>  The OpenType language (such as "ROM ", "URD ", and "FAR " for Romanian, Urdu, and Persian) are determined from the locale, and the script ("latn" and "arab" for Latin and Arabic) is determined from the script analyzer. That's why these are not listed under OpenType tags, only the feature tags</div>
<div> </div>

#### Examples

Example: <b>DWRITE_MAKE_OPENTYPE_TAG</b>('c','c','m','p')
 

Dword:   0x706D6363

<div class="code"></div>


