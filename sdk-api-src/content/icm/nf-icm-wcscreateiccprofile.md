---
UID: NF:icm.WcsCreateIccProfile
title: WcsCreateIccProfile function
author: windows-sdk-content
description: Converts a WCS profile into an International Color Consortium (ICC) profile.
old-location: wcs\wcscreateiccprofile.htm
tech.root: WCS
ms.assetid: 6e9aaad6-a7d4-4685-b694-89d499a411e1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WcsCreateIccProfile, WcsCreateIccProfile function [Windows Color System], _color_WcsCreateIccProfile, icm/WcsCreateIccProfile, wcs.wcscreateiccprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - WcsCreateIccProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsCreateIccProfile function


## -description


Converts a WCS profile into an International Color Consortium (ICC) profile.


## -parameters




### -param hWcsProfile [in]

A handle to the WCS color profile that is converted. See Remarks.


### -param dwOptions [in]

A flag value that specifies the profile conversion options.<div> </div>
<div> </div>By default, the original WCS profiles used for the conversion are embedded in the output ICC profile in a Microsoft private tag, <i>WcsProfilesTag</i> (with signature "MS000". This produces an ICC profile that is compatible with ICC software, yet retains the original WCS profile data available to code designed to parse it.<div> </div>
<div> </div>The possible values of this parameter are as follows. Any bits not defined in this list are reserved and should be set to zero:

<table>
<tr>
<td>WCS_DEFAULT</td>
<td>Specifies that the new ICC profile contains the original WCS profile in a private WcsProfilesTag.</td>
</tr>
<tr>
<td>WCS_ICCONLY</td>
<td>Specifies that the new ICC profile does not contain either the WcsProfilesTag or the original WCS profile.</td>
</tr>
</table>
 


## -returns



If this function succeeds, the return value is the handle of the new color profile.

If this function fails, the return value is <b>NULL</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can be used with ASCII or Unicode strings.

The <b>CloseColorProfile</b> function should be used to close the returned HPROFILE handle when it is no longer needed.

The DMP, CAMP, and GMMP from the HPROFILE are embedded in a private tag within the created ICC profile.

The ICC profile created using this API will have its profile description tag constructed from the ProfileName elements of the WCS profiles according to the following pattern: "Created by Microsoft WCS from DMP:[the DMP ProfileName], CAMP:[the CAMP ProfileName], GMMP:[the GMMP ProfileName]"

When WCS encounters this ICC profile (via <a href="https://msdn.microsoft.com/5f738012-690f-4ff9-bc40-4ccbd47169c6">OpenColorProfile</a> or <a href="https://msdn.microsoft.com/4ceb81d0-dc43-46dd-a455-ec00c8e2140c">WcsOpenColorProfile</a> ) it extracts and uses the WCS profile(s) contained in the <i>WcsProfilesTag</i>.

The out-of-gamut information in the gamut tags created in WCS uses the perceptual color distance in CIECAM02, which is the mean square root in CIECAM02 Jab space. The distance in legacy ICC profile gamut tags is the mean square root in CIELAB space. It is recommended that you use the CIECAM02 space when it is available, to provide more perceptually accurate distance metrics.

WCS extracts and uses the original WCS profile by means of an XML profile explicitly associated with a device, or an ICC profile that has a<i>WcsProfilesTag</i>.

The <i>WcsProfilesTag</i> is a Microsoft private ICC profile tag used in profiles created by <b>WcsCreateIccProfile</b> to contain the WCS profiles input to <b>WcsCreateIccProfile</b>. This tag conforms to ICC profile requirements for profile tags. The non-XML components of the tag must be in "Big-Endian" byte ordering, which is standard for ICC profiles. Further, the tag data must be aligned on a 4-byte boundary (measured from the start of the ICC profile). The structure of the tag is defined by the <b>WcsProfilesTagType</b> below. Note that the XML components of the tag, the WCS profiles contained in the WcsProfileTag, are left in their native byte ordering, which may be either little-endian or big-endian since XML parsers correctly process either.

The WcsProfilesTag signature is "MS00". This is the tag signature that will appear in the ICC profiles tag table for the WcsProfilesTag.

The <b>WcsProfilesTagType Structure</b> has the following structure:

<table>
<tr>
<th>Byte Offset</th>
<th>Content</th>
</tr>
<tr>
<td>0-3 </td>
<td>The MS10 type signature.</td>
</tr>
<tr>
<td>4-7</td>
<td>Reserved, must be set to 0 (ICC tradition).</td>
</tr>
<tr>
<td>8-11 </td>
<td>Byte offset from the beginning of the tag to the CDMP data.</td>
</tr>
<tr>
<td>12-15 </td>
<td>  Size of the CDMP data in bytes. </td>
</tr>
<tr>
<td>16-19 </td>
<td>  Byte offset from the beginning of the tag to the CAMP data.</td>
</tr>
<tr>
<td>20-23 </td>
<td>Size of the CAMP data in bytes.</td>
</tr>
<tr>
<td>24-27</td>
<td>Byte offset from the beginning of the tag to the GMMP data.</td>
</tr>
<tr>
<td>28-31</td>
<td>Byte offset from the beginning of the tag to the GMMP data.</td>
</tr>
<tr>
<td>31-n </td>
<td>A sequence of (element size -32) bytes [where element size is the tag size recorded in the ICC profile tag table entry for this tag.]</td>
</tr>
</table>
 

These are the WCS XML profiles that were used by <b>WcsCreateIccProfile</b> to create this ICC profile. The WCS profiles are ordered: the DMP (required) first, followed by the CAMP (if present), followed by the GMMP (if present).




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

