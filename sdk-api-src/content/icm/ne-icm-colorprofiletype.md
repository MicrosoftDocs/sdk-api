---
UID: NE:icm.COLORPROFILETYPE
title: COLORPROFILETYPE
description: Specifies the type of color profile.
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
 - COLORPROFILETYPE
f1_keywords:
 - COLORPROFILETYPE
 - icm/COLORPROFILETYPE
dev_langs:
 - c++
---

## -description

Specifies the type of color profile.

## -enum-fields

### -field CPT_ICC

An International Color Consortium (ICC) profile. If you specify this value, only the CPST\_RGB\_WORKING\_SPACE and CPST\_CUSTOM\_WORKING\_SPACE values of [**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype) are valid.

### -field CPT_DMP

A device model profile (DMP) defined in WCS. If you specify this value, only the CPST\_RGB\_WORKING\_SPACE and CPST\_CUSTOM\_WORKING\_SPACE values of [**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype) are valid.

### -field CPT_CAMP

A color appearance model profile (CAMP) defined in WCS. If you specify this value, only the CPST\_NONE value of [**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype) is valid.

### -field CPT_GMMP

Specifies a WCS gamut map model profile (GMMP). If this value is specified, only the CPST\_PERCEPTUAL, CPST\_SATURATION, CPST\_RELATIVE\_COLORIMETRIC, and CPST\_ABSOLUTE\_COLORIMETRIC values of [**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype) are valid. Any of these values may optionally be combined (in a bitwise **OR** operation) with CPST\_DEFAULT.

## -remarks

The PCOLORPROFILETYPE and LPCOLORPROFILETYPE data types are defined as pointers to this enumeration:

`typedef COLORPROFILETYPE *PCOLORPROFILETYPE, *LPCOLORPROFILETYPE;`

## -see-also

[**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

