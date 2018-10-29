---
UID: NE:icm.COLORDATATYPE
title: COLORDATATYPE
author: windows-sdk-content
description: Used by WCS functions to indicate the data type of vector content.
old-location: wcs\colordatatype.htm
tech.root: WCS
ms.assetid: 001001c2-9a34-4d70-937d-befa0fc2118c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCOLORDATATYPE, COLORDATATYPE, COLORDATATYPE enumeration [Windows Color System], COLOR_10b_R10G10B10A2, COLOR_10b_R10G10B10A2_XR, COLOR_BYTE, COLOR_FLOAT, COLOR_S2DOT13FIXED, COLOR_WORD, LPCOLORDATATYPE, LPCOLORDATATYPE enumeration pointer [Windows Color System], PCOLORDATATYPE, PCOLORDATATYPE enumeration pointer [Windows Color System], icm/COLORDATATYPE, icm/COLOR_10b_R10G10B10A2, icm/COLOR_10b_R10G10B10A2_XR, icm/COLOR_BYTE, icm/COLOR_FLOAT, icm/COLOR_S2DOT13FIXED, icm/COLOR_WORD, icm/LPCOLORDATATYPE, icm/PCOLORDATATYPE, wcs.colordatatype"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Icm.h
api_name:
 - COLORDATATYPE
product: Windows
targetos: Windows
req.typenames: COLORDATATYPE
req.redist: 
---

# COLORDATATYPE enumeration


## -description


Used by WCS functions to indicate the data type of vector content.


## -enum-fields




### -field COLOR_BYTE

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

Color data is stored as 10 bits per channel, 32 bits per pixel.  The 10 bits of each color channel are 2.8 fixed point with a -0.75 bias, giving a range of [-0.76 .. 1.25]. This range corresponds to [-0.5 .. 1.5] in a gamma = 1 space. The two most significant bits are preserved for alpha.

This uses an extended range (XR) sRGB color space. It has the same RGB primaries, white point, and gamma as sRGB.


### -field COLOR_FLOAT16




## -remarks



The PCOLORDATATYPE and LPCOLORDATATYPE data types are defined as pointers to the <b>COLORDATATYPE</b> enumeration:

<code>typedef COLORDATATYPE *PCOLORDATATYPE, *LPCOLORDATATYPE;</code>



