---
UID: NS:icm.tagPROFILEHEADER
title: PROFILEHEADER
description: Contains information that describes the contents of a device profile file. This header occurs at the beginning of a device profile file.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.typenames: PROFILEHEADER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - tagPROFILEHEADER
 - PROFILEHEADER
f1_keywords:
 - tagPROFILEHEADER
 - icm/tagPROFILEHEADER
 - PROFILEHEADER
 - icm/PROFILEHEADER
dev_langs:
 - c++
---

## -description

Contains information that describes the contents of a device profile file. This header occurs at the beginning of a device profile file.

## -struct-fields

### -field phSize

The size of the profile in bytes.

### -field phCMMType

The identification number of the CMM that is used in the profile. Identification numbers are registered with the ICC.

### -field phVersion

The version number of the profile. The version number is determined by the ICC. The current major version number is 02h. The current minor version number is 10h. The major and minor version numbers are in binary coded decimal (BCD). They must be stored in the following format.

| Byte Number | Contents                                                                                                                  |
|-------------|---------------------------------------------------------------------------------------------------------------------------|
| 0           | Major version number in BCD.                                                                                              |
| 1           | Minor version number in the most significant nibble of this byte. Bug fix version number in the least significant nibble. |
| 2           | Reserved. Must be set to 0.                                                                                               |
| 3           | Reserved. Must be set to 0.                                                                                               |

### -field phClass

Indicates the profile class. For a description of profile classes, see [Using Device Profiles with WCS](/windows/win32/wcs/using-device-profiles-with-wcs). A profile class may have any of the following values.

| Profile Class                  | Signature         |
|--------------------------------|-------------------|
| Input Device Profile           | CLASS\_SCANNER    |
| Display Device Profile         | CLASS\_MONITOR    |
| Output Device Profile          | CLASS\_PRINTER    |
| Device Link Profile            | CLASS\_LINK       |
| Color Space Conversion Profile | CLASS\_COLORSPACE |
| Abstract Profile               | CLASS\_ABSTRACT   |
| Named Color Profile            | CLASS\_NAMED      |
| Color Appearance Model Profile | CLASS\_CAMP       |
| Color Gamut Map Model Profile  | CLASS\_GMMP       |

### -field phDataColorSpace

A signature value that indicates the color space in which the profile data is defined. The member can be any of value from the [Color Space Constants](/windows/win32/wcs/color-space-constants).

### -field phConnectionSpace

A signature value that indicates the color space in which the profile connection space (PCS) is defined. The member can be any of the following values.

| Profile Class | Signature  |
|---------------|------------|
| XYZ           | SPACE\_XYZ |
| Lab           | SPACE\_Lab |

When the **phClass** member is set to CLASS\_LINK, the PCS is taken from the **phDataColorSpace** member.

### -field phDateTime

The date and time that the profile was created.

### -field phSignature

Reserved for internal use.

### -field phPlatform

The primary platform for which the profile was created. The primary platform can be set to any of the following values.

| Platform               | Value  |
|------------------------|--------|
| Apple Computer, Inc.   | 'APPL' |
| Microsoft Corp.        | 'MSFT' |
| Silicon Graphics, Inc. | 'SGI'  |
| Sun Microsystems, Inc. | 'SUNW' |
| Taligent               | 'TGNT' |

### -field phProfileFlags

Bit flags containing hints that the CMM uses to interpret the profile data. The member can be set to the following values.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Constant</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
<table>
<tbody>
<tr class="odd">
<td>FLAG_EMBEDDEDPROFILE</td>

</tr>
</tbody>
</table>

<p> </p></td>
<td>
<table>
<tbody>
<tr class="odd">
<td>The profile is embedded in a bitmap file.</td>

</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>
<table>
<tbody>
<tr class="odd">
<td>FLAG_DEPENDENTONDATA</td>

</tr>
</tbody>
</table>

<p> </p></td>
<td>
<table>
<tbody>
<tr class="odd">
<td>The profile can't be used independently of the embedded color data. Used for profiles that are embedded in bitmap files.</td>

</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

### -field phManufacturer

The identification number of the device profile manufacturer. All manufacturer identification numbers are registered with the ICC.

### -field phModel

The device manufacturer's device model number. All model identification numbers are registered with the ICC.

### -field phAttributes

Attributes of profile. The profile attributes can be any of the following values.

| Constant             | Meaning                                                                                  |
|----------------------|------------------------------------------------------------------------------------------|
| ATTRIB\_TRANSPARENCY | Turns transparency on. If this flag is not used, the attribute is reflective by default. |
| ATTRIB\_MATTE        | Turns matte display on. If this flag is not used, the attribute is glossy by default.    |

### -field phRenderingIntent

The profile rendering intent. The member can be set to one of the following values:

INTENT\_PERCEPTUAL

INTENT\_SATURATION

INTENT\_RELATIVE\_COLORIMETRIC

INTENT\_ABSOLUTE\_COLORIMETRIC

For more information, see [Rendering intents](/windows/win32/wcs/rendering-intents).

### -field phIlluminant

Profile illuminant.

### -field phCreator

Signature of the software that created the profile. Signatures are registered with the ICC.

### -field phReserved

Reserved.

## -remarks

## -see-also

* [Further information](/windows/win32/wcs/further-information)
* [Using device profiles with WCS](/windows/win32/wcs/using-device-profiles-with-wcs)
* [Rendering intents](/windows/win32/wcs/rendering-intents)
