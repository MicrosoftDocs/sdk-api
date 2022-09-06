---
UID: NE:icm.__unnamed_enum_3
title: COLORDATATYPE
description: Used by WCS functions to indicate the data type of vector content.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Vista \[desktop apps only\]
req.target-min-winversvr: Windows Server 2008 \[desktop apps only\]
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - COLORDATATYPE
f1_keywords:
 - COLORDATATYPE
 - icm/COLORDATATYPE
dev_langs:
 - c++
---

## -description

Used by WCS functions to indicate the data type of vector content.

## -enum-fields

### -field COLOR_BYTE:1

Color data is stored as 8 bits per channel, with a value from 0 to 255, inclusive.

### -field COLOR_WORD

Color data is stored as 16 bits per channel, with a value from 0 to 65535, inclusive.

### -field COLOR_FLOAT

Color data is stored as 32 bits value per channel, as defined by the IEEE 32-bit floating point standard.

### -field COLOR_S2DOT13FIXED

Color data is stored as 16 bits per channel, with a fixed range of -4 to +4, inclusive. A signed format is used, with 1 bit for the sign, 2 bits for the integer portion, and 13 bits for the fractional portion.

### -field COLOR_10b_R10G10B10A2

Color data is stored as 10 bits per channel. The two most significant bits are alpha.

### -field COLOR_10b_R10G10B10A2_XR

Color data is stored as 10 bits per channel, 32 bits per pixel. The 10 bits of each color channel are 2.8 fixed point with a -0.75 bias, giving a range of \[-0.76 .. 1.25\]. This range corresponds to \[-0.5 .. 1.5\] in a gamma = 1 space. The two most significant bits are preserved for alpha.

This uses an extended range (XR) sRGB color space. It has the same RGB primaries, white point, and gamma as sRGB.

### -field COLOR_FLOAT16

Color data is stored as 16 bits value per channel, as defined by the IEEE 16-bit floating point standard.

## -remarks

The PCOLORDATATYPE and LPCOLORDATATYPE data types are defined as pointers to the **COLORDATATYPE** enumeration:

`typedef COLORDATATYPE *PCOLORDATATYPE, *LPCOLORDATATYPE;`

## -see-also
