---
UID: NF:dwrite.DWRITE_MAKE_OPENTYPE_TAG
title: DWRITE_MAKE_OPENTYPE_TAG macro (dwrite.h)
description: Creates an OpenType tag as a 32-bit integer, such that the first character in the tag is the lowest byte (least significant on little endian architectures), which can be used to compare with tags in the font file.
helpviewer_keywords: ["DWRITE_MAKE_OPENTYPE_TAG","DWRITE_MAKE_OPENTYPE_TAG macro [Direct Write]","directwrite.dwrite_make_opentype_tag","dwrite/DWRITE_MAKE_OPENTYPE_TAG"]
old-location: directwrite\dwrite_make_opentype_tag.htm
tech.root: DirectWrite
ms.assetid: fe93a24a-5f3d-4e73-87ac-b33357c838e3
ms.date: 07/01/2025
ms.keywords: DWRITE_MAKE_OPENTYPE_TAG, DWRITE_MAKE_OPENTYPE_TAG macro [Direct Write], directwrite.dwrite_make_opentype_tag, dwrite/DWRITE_MAKE_OPENTYPE_TAG
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - DWRITE_MAKE_OPENTYPE_TAG
 - dwrite/DWRITE_MAKE_OPENTYPE_TAG
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
 - DWRITE_MAKE_OPENTYPE_TAG
---

# DWRITE_MAKE_OPENTYPE_TAG macro

## -syntax

```cpp
DWORD DWRITE_MAKE_OPENTYPE_TAG(
    char a,
    char b,
    char c,
    char d
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

An OpenType tag as a 32-bit integer.


## -description

Creates an OpenType tag as a 32-bit integer, such that the first character in the tag is the lowest byte (least significant on little-endian architectures), which can be used to compare with tags in the font file. This macro is compatible with [DWRITE_FONT_FEATURE_TAG](./ne-dwrite-dwrite_font_feature_tag.md).

## -parameters

### -param a

Type: **[CHAR](/windows/win32/winprog/windows-data-types)**

The first character in the tag.

### -param b

Type: **[CHAR](/windows/win32/winprog/windows-data-types)**

The second character in the tag.

### -param c

Type: **[CHAR](/windows/win32/winprog/windows-data-types)**

The third character in the tag.

### -param d

Type: **[CHAR](/windows/win32/winprog/windows-data-types)**

The fourth character in the tag.

## -remarks

The OpenType language (such as "ROM ", "URD ", and "FAR " for Romanian, Urdu, and Persian) are determined from the locale, and the script ("latn" and "arab" for Latin and Arabic) is determined from the script analyzer. That's why these are not listed under OpenType tags; only the feature tags.

## Examples

```cpp
DWRITE_MAKE_OPENTYPE_TAG('c','c','m','p');
// Result: DWORD 0x706D6363
```
