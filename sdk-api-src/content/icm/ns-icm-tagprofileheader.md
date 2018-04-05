---
UID: NS:icm.tagPROFILEHEADER
title: tagPROFILEHEADER
author: windows-driver-content
description: The PROFILEHEADER structure contains information that describes the contents of a device profile file. This header occurs at the beginning of a device profile file.
old-location: wcs\profileheader.htm
old-project: WCS
ms.assetid: bf17bd8a-6ab5-45f8-89c3-797dd090dd6f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PPROFILEHEADER, PROFILEHEADER, PROFILEHEADER structure [Windows Color System], _color_PROFILEHEADER_str, icm/PROFILEHEADER, tagPROFILEHEADER, wcs.profileheader"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROFILEHEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Icm.h
api_name:
-	PROFILEHEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagPROFILEHEADER structure


## -description



The <b>PROFILEHEADER</b> structure contains information that describes the contents of a device profile file. This header occurs at the beginning of a device profile file.




## -struct-fields




### -field phSize

The size of the profile in bytes.


### -field phCMMType

The identification number of the CMM that is used in the profile. Identification numbers are registered with the ICC.


### -field phVersion

The version number of the profile. The version number is determined by the ICC. The current major version number is 02h. The current minor version number is 10h. The major and minor version numbers are in binary coded decimal (BCD). They must be stored in the following format.

<table>
<tr>
<th>Byte Number</th>
<th>Contents</th>
</tr>
<tr>
<td>0</td>
<td>Major version number in BCD.</td>
</tr>
<tr>
<td>1</td>
<td>Minor version number in the most significant nibble of this byte. Bug fix version number in the least significant nibble.</td>
</tr>
<tr>
<td>2</td>
<td>Reserved. Must be set to 0.</td>
</tr>
<tr>
<td>3</td>
<td>Reserved. Must be set to 0.</td>
</tr>
</table>
 


### -field phClass

Indicates the profile class. For a description of profile classes, see <a href="https://msdn.microsoft.com/9ea420ad-dcf1-4ba9-b739-308be7a56a6c">Using Device Profiles with WCS</a>. A profile class may have any of the following values.

<table>
<tr>
<th>Profile Class</th>
<th>Signature</th>
</tr>
<tr>
<td>Input Device Profile</td>
<td>CLASS_SCANNER</td>
</tr>
<tr>
<td>Display Device Profile</td>
<td>CLASS_MONITOR</td>
</tr>
<tr>
<td>Output Device Profile</td>
<td>CLASS_PRINTER</td>
</tr>
<tr>
<td>Device Link Profile</td>
<td>CLASS_LINK</td>
</tr>
<tr>
<td>Color Space Conversion Profile</td>
<td>CLASS_COLORSPACE</td>
</tr>
<tr>
<td>Abstract Profile</td>
<td>CLASS_ABSTRACT</td>
</tr>
<tr>
<td>Named Color Profile</td>
<td>CLASS_NAMED</td>
</tr>
<tr>
<td>Color Appearance Model Profile</td>
<td>CLASS_CAMP</td>
</tr>
<tr>
<td>Color Gamut Map Model Profile</td>
<td>CLASS_GMMP</td>
</tr>
</table>
 


### -field phDataColorSpace

A signature value that indicates the color space in which the profile data is defined. The member can be any of value from the <a href="https://msdn.microsoft.com/714c122f-3d68-4466-900c-1d129e544d45">Color Space Constants</a>.


### -field phConnectionSpace

A signature value that indicates the color space in which the profile connection space (PCS) is defined. The member can be any of the following values.

<table>
<tr>
<th>Profile Class</th>
<th>Signature</th>
</tr>
<tr>
<td>XYZ</td>
<td>SPACE_XYZ</td>
</tr>
<tr>
<td>Lab</td>
<td>SPACE_Lab</td>
</tr>
</table>
 

When the <b>phClass</b> member is set to CLASS_LINK, the PCS is taken from the <b>phDataColorSpace</b> member.


### -field phDateTime

The data and time that the profile was created.


### -field phSignature

Reserved for internal use.


### -field phPlatform

The primary platform for which the profile was created. The primary platform can be set to any of the following values.

<table>
<tr>
<th>Platform</th>
<th>Value</th>
</tr>
<tr>
<td>Apple Computer, Inc.</td>
<td>'APPL'</td>
</tr>
<tr>
<td>Microsoft Corp.</td>
<td>'MSFT'</td>
</tr>
<tr>
<td>Silicon Graphics, Inc.</td>
<td>'SGI'</td>
</tr>
<tr>
<td>Sun Microsystems, Inc.</td>
<td>'SUNW'</td>
</tr>
<tr>
<td>Taligent</td>
<td>'TGNT'</td>
</tr>
</table>
 


### -field phProfileFlags

Bit flags containing hints that the CMM uses to interpret the profile data. The member can be set to the following values.

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<table>
<tr>
<td>FLAG_EMBEDDEDPROFILE</td>
<td></td>
</tr>
</table>
 

</td>
<td>
<table>
<tr>
<td>The profile is embedded in a bitmap file.</td>
<td></td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td>
<table>
<tr>
<td>FLAG_DEPENDENTONDATA</td>
<td></td>
</tr>
</table>
 

</td>
<td>
<table>
<tr>
<td>The profile can't be used independently of the embedded color data. Used for profiles that are embedded in bitmap files.</td>
<td></td>
</tr>
</table>
 

</td>
</tr>
</table>
 


### -field phManufacturer

The identification number of the device profile manufacturer. All manufacturer identification numbers are registered with the ICC.


### -field phModel

The device manufacturer's device model number. All model identification numbers are registered with the ICC.


### -field phAttributes

Attributes of profile. The profile attributes can be any of the following values.

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>ATTRIB_TRANSPARENCY</td>
<td>Turns transparency on. If this flag is not used, the attribute is reflective by default.</td>
</tr>
<tr>
<td>ATTRIB_MATTE</td>
<td>Turns matte display on. If this flag is not used, the attribute is glossy by default.</td>
</tr>
</table>
 


### -field phRenderingIntent

The profile rendering intent. The member can be set to one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -field phIlluminant

Profile illuminant.


### -field phCreator

Signature of the software that created the profile. Signatures are registered with the ICC.


### -field phReserved

Reservedfuture.


## -see-also




<a href="https://msdn.microsoft.com/6e2ac851-3dba-4bbb-b766-82800b1cc5f1">Further Information</a>



<a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>



<a href="https://msdn.microsoft.com/9ea420ad-dcf1-4ba9-b739-308be7a56a6c">Using Device Profiles with WCS</a>
 

 

