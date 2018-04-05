---
UID: NE:icm.COLORPROFILESUBTYPE
title: COLORPROFILESUBTYPE
author: windows-driver-content
description: Specifies the subtype of the color profile.
old-location: wcs\colorprofilesubtype.htm
old-project: WCS
ms.assetid: b5cc965e-47b2-4309-8558-5208c7a2b587
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PCOLORPROFILESUBTYPE, COLORPROFILESUBTYPE, COLORPROFILESUBTYPE PCOLORPROFILESUBTYPE, COLORPROFILESUBTYPE PCOLORPROFILESUBTYPE enumeration pointer [Windows Color System], COLORPROFILESUBTYPE enumeration [Windows Color System], COLORPROFILSUBTYPE, COLORPROFILSUBTYPE enumeration [Windows Color System], CPST_ABSOLUTE_COLORIMETRIC, CPST_CUSTOM_WORKING_SPACE, CPST_NONE, CPST_PERCEPTUAL, CPST_RELATIVE_COLORIMETRIC, CPST_RGB_WORKING_SPACE, CPST_SATURATION, LPCOLORPROFILESUBTYPE, LPCOLORPROFILESUBTYPE enumeration pointer [Windows Color System], icm/COLORPROFILESUBTYPE, icm/COLORPROFILESUBTYPE PCOLORPROFILESUBTYPE, icm/CPST_ABSOLUTE_COLORIMETRIC, icm/CPST_CUSTOM_WORKING_SPACE, icm/CPST_NONE, icm/CPST_PERCEPTUAL, icm/CPST_RELATIVE_COLORIMETRIC, icm/CPST_RGB_WORKING_SPACE, icm/CPST_SATURATION, icm/LPCOLORPROFILESUBTYPE, wcs.colorprofilesubtype"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: COLORPROFILESUBTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Icm.h
api_name:
-	COLORPROFILSUBTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# COLORPROFILESUBTYPE enumeration


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


### -field CPST_EXTENDED_DISPLAY_COLOR_MODE




## -remarks



For a description of rendering intents, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.

The PCOLORPROFILESUBTYPE and LPCOLORPROFILESUBTYPE data types are defined as pointers to the <b>COLORPROFILESUBTYPE</b> enumeration:

<code>typedef COLORPROFILESUBTYPE *PCOLORPROFILESUBTYPE, *LPCOLORPROFILESUBTYPE;</code>

The valid profile type/subtype combinations are

<table>
<tr>
<td rowspan="3">
COLORPROFILETYPE

</td>
<td colspan="4">
Valid COLORPROFILESUBTYPE

</td>
<td rowspan="3">
Notes

</td>
</tr>
<tr>
<td colspan="2">
default for a device

</td>
<td colspan="2">
global default

</td>
</tr>
<tr>
<td>


</td>
<td>
Intended Usage

</td>
<td>


</td>
<td>
Intended Usage

</td>
</tr>
<tr>
<td>
CPT_ICC



</td>
<td>
CPST_NONE

</td>
<td>
Get/Set default ICC profile associated with a device

</td>
<td>
CPST_RGBWorkingSpace or CPST_CustomWorkingSpace

</td>
<td>
Get/Set ICC profile as global RGB or custom working space

</td>
<td>


</td>
</tr>
<tr>
<td>
CPT_DMP

</td>
<td>
CPST_NONE

</td>
<td>
Get/Set default DMP profile associated with a device

</td>
<td>
CPST_RGBWorkingSpace or CPST_CustomWorkingSpace

</td>
<td>
Get/Set DMP as global RGB or custom working space

</td>
<td>


</td>
</tr>
<tr>
<td>
CPT_CAMP

</td>
<td>
CPST_NONE

</td>
<td>
Get/Set default CAMP profile associated with a device

</td>
<td>
CPST_NONE

</td>
<td>
Get/Set CAMP profile as global color appearance profile

</td>
<td>


</td>
</tr>
<tr>
<td>
CPT_GMMP

</td>
<td>
CPST_NONE

</td>
<td>
Get/Set default GMMP profile associated with a device

</td>
<td>
CPST_Perceptual or

CPST_Absolute_colorimetric or

CPST_Relative_colorimetric or

CPTS_Saturation

</td>
<td>
Get/Set GMMP as global gamut map model profile for a specific rendering intent as described by that subtype to be used in CreateMultiProfileTransform API when resolving the rendering intent array in WCS transform.

</td>
<td>
COLORPROFILESUBTYPE Global default can be or?d with WCS_DEFAULT to set this GMMP as the global default for use in OpenColorProfile or WcsOpenColorProfile where GMMP is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546018">COLORPROFILETYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563739">WcsSetDefaultColorProfile</a>
 

 

