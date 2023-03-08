---
UID: NE:icm.COLORPROFILESUBTYPE
title: COLORPROFILESUBTYPE
description: Specifies the subtype of the color profile.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
 - COLORPROFILESUBTYPE
f1_keywords:
 - COLORPROFILESUBTYPE
 - icm/COLORPROFILESUBTYPE
dev_langs:
 - c++
---

## -description

Specifies the subtype of the color profile.

## -enum-fields

### -field CPST_PERCEPTUAL

A perceptual rendering intent for gamut map model profiles (GMMPs) defined in WCS.

### -field CPST_RELATIVE_COLORIMETRIC

A relative colorimetric rendering intent for GMMPs defined in WCS.

### -field CPST_SATURATION

A saturation rendering intent for GMMPs defined in WCS.

### -field CPST_ABSOLUTE_COLORIMETRIC

An absolute colorimetric rendering intent for GMMPs defined in WCS.

### -field CPST_NONE

The color profile subtype is not applicable to the selected color profile type.

### -field CPST_RGB_WORKING_SPACE

The RGB color working space for International Color Consortium (ICC) profiles or device model profiles (DMPs) defined in WCS.

### -field CPST_CUSTOM_WORKING_SPACE

A custom color working space.

### -field CPST_STANDARD_DISPLAY_COLOR_MODE

TBD

### -field CPST_EXTENDED_DISPLAY_COLOR_MODE

TBD

## -remarks

For a description of rendering intents, see [Rendering Intents](/windows/win32/wcs/rendering-intents).

The PCOLORPROFILESUBTYPE and LPCOLORPROFILESUBTYPE data types are defined as pointers to the **COLORPROFILESUBTYPE** enumeration:

`typedef COLORPROFILESUBTYPE *PCOLORPROFILESUBTYPE, *LPCOLORPROFILESUBTYPE;`

The valid profile type/subtype combinations are

${ROWSPAN3}$ COLORPROFILETYPE<br/> ${REMOVE}$  

Valid COLORPROFILESUBTYPE<br/>

${ROWSPAN3}$ Notes<br/> ${REMOVE}$  

default for a device<br/>

global default<br/>

Intended Usage<br/>

Intended Usage<br/>

CPT\_ICC<br/>

CPST\_NONE<br/>

Get/Set default ICC profile associated with a device<br/>

CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace<br/>

Get/Set ICC profile as global RGB or custom working space<br/>

CPT\_DMP<br/>

CPST\_NONE<br/>

Get/Set default DMP profile associated with a device<br/>

CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace<br/>

Get/Set DMP as global RGB or custom working space<br/>

CPT\_CAMP<br/>

CPST\_NONE<br/>

Get/Set default CAMP profile associated with a device<br/>

CPST\_NONE<br/>

Get/Set CAMP profile as global color appearance profile<br/>

CPT\_GMMP<br/>

CPST\_NONE<br/>

Get/Set default GMMP profile associated with a device<br/>

CPST\_Perceptual or<br/> CPST\_Absolute\_colorimetric or<br/> CPST\_Relative\_colorimetric or<br/> CPTS\_Saturation<br/>

Get/Set GMMP as global gamut map model profile for a specific rendering intent as described by that subtype to be used in CreateMultiProfileTransform API when resolving the rendering intent array in WCS transform.<br/>

COLORPROFILESUBTYPE Global default can be or?d with WCS\_DEFAULT to set this GMMP as the global default for use in OpenColorProfile or WcsOpenColorProfile where GMMP is **NULL**.<br/>

## -see-also

* [**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype)
* [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

