---
UID: NS:wcsplugin._BlackInformation
title: "_BlackInformation"
author: windows-sdk-content
description: Contains information for device models that have a black color channel.
old-location: wcs\blackinformation.htm
old-project: WCS
ms.assetid: b90699f6-b42e-4848-947b-76633dc35802
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: BlackInformation, BlackInformation structure [Windows Color System], _BlackInformation, _color_BlackInformation_str, wcs.blackinformation, wcsplugin/BlackInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wcsplugin.h
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
tech.root: 
req.typenames: BlackInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcsPlugIn.h
api_name:
 - BlackInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _BlackInformation structure


## -description



Contains information for device models that have a black color channel.




## -struct-fields




### -field fBlackOnly

 


### -field blackWeight

A value between 0.0 and 1.0 that indicates the relative amount of black to use in the output. A value of 0.0 means that no black is used; a value of 1.0 means that the maximum amount of black is used.


#### - bBlackOnly

An indicator whether the source color contains only black. This value can only be true if both of the following apply:

<ul>
<li>the source device has a black channel</li>
<li>the <a href="_color_cmm_transform_creation_flags">PRESERVEBLACK</a> flag is set to <b>true</b>. This flag is in the <i>dwFlags</i> parameter of a Color Management Module (CMM) transform function.</li>
</ul>

## -remarks



If the source device does not support a black channel, then WCS sets <b>bBlackOnly</b> to <b>FALSE</b>.

If <b>bBlackOnly</b> is <b>TRUE</b>, then WCS generates an output device control value where, at most, the black channel will be non-zero. This only happens if the <b>BlackPreservation</b> flag was set in WCS. Note that in such cases, the device model may not be providing the closest colorimetric match to the supplied value.

Black preservation is only performed when both the source and destination devices support a black channel. If black is being preserved with these devices, then for each source device control value, where all channels other than the black channel are zero, the <b>bBlackOnly</b> flag is <b>TRUE</b>. Note that this means that a value where all channels are zero will also set <b>bBlackOnly</b> to <b>TRUE</b>.

<b>blackWeight</b> gives us information about the device control values used in the source device.

<ul>
<li>For source devices with a black channel, <b>blackWeight</b> is set to the black value.</li>
<li>For source devices without a black channel, the black weight is computed using a combination of <i>color purity</i> and <i>relative lightness</i>.<i>Color purity</i>is defined as (maxColorant - minColorant)/maxColorant

<i>Relative lightness</i> is defined as (the lightness of the color in appearance space - minimum lightness of destination device) / (maximum lightness of destination device - minimum lightness of destination device)

For RGB devices, blackWeight = (1 - colorPurity) * (1 - relativeLightness)
      
      

For CMYK devices, blackWeight = colorPurity * (1 - relativeLightness)

WCS is responsible for initializing the <b>BlackInformation</b> structure. 

</li>
</ul>
If <b>bBlackOnly</b> is <b>FALSE</b>, then the baseline device models for devices with a black channel will use the <b>blackWeight</b> to guide the creation of a colorimetrically appropriate output pixel value. For CMYK devices, <b>blackWeight</b> provides WCS's initial estimation of a K value and it searches for C, M, and Y values that will lead to the correct colorimetry. If it does not find a match, it adjusts the K value and searches again.

You can set plug-ins to either support or ignore the <b>BlackInformation</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

