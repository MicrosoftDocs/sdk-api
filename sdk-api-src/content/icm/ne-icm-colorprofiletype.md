---
UID: NE:icm.COLORPROFILETYPE
title: COLORPROFILETYPE
author: windows-sdk-content
description: Specifies the type of color profile.
old-location: wcs\colorprofiletype.htm
tech.root: WCS
ms.assetid: aaf6fd19-0693-4a76-812f-ff958eb5c944
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PCOLORPROFILETYPE, COLORPROFILETYPE, COLORPROFILETYPE enumeration [Windows Color System], CPT_CAMP, CPT_DMP, CPT_GMMP, CPT_ICC, LPCOLORPROFILETYPE, LPCOLORPROFILETYPE enumeration pointer [Windows Color System], PCOLORPROFILETYPE, PCOLORPROFILETYPE enumeration pointer [Windows Color System], icm/COLORPROFILETYPE, icm/CPT_CAMP, icm/CPT_DMP, icm/CPT_GMMP, icm/CPT_ICC, icm/LPCOLORPROFILETYPE, icm/PCOLORPROFILETYPE, wcs.colorprofiletype"
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
 - COLORPROFILETYPE
product: Windows
targetos: Windows
req.typenames: COLORPROFILETYPE
req.redist: 
---

# COLORPROFILETYPE enumeration


## -description


Specifies the type of color profile.


## -enum-fields




### -field CPT_ICC

An International Color Consortium (ICC) profile. If you specify this value, only the CPST_RGB_WORKING_SPACE and CPST_CUSTOM_WORKING_SPACE values of <a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a> are valid.


### -field CPT_DMP

A device model profile (DMP) defined in WCS. If you specify this value, only the CPST_RGB_WORKING_SPACE and CPST_CUSTOM_WORKING_SPACE values of <a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a> are valid.


### -field CPT_CAMP

A color appearance model profile (CAMP) defined in WCS. If you specify this value, only the CPST_NONE value of <a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a> is valid.


### -field CPT_GMMP

Specifies a WCS gamut map model profile (GMMP). If this value is specified, only the CPST_PERCEPTUAL, CPST_SATURATION, CPST_RELATIVE_COLORIMETRIC, and CPST_ABSOLUTE_COLORIMETRIC values of <a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a> are valid. Any of these values may optionally be combined (in a bitwise <b>OR</b> operation) with CPST_DEFAULT.


## -remarks



The PCOLORPROFILETYPE and LPCOLORPROFILETYPE data types are defined as pointers to this enumeration:

<code>typedef COLORPROFILETYPE *PCOLORPROFILETYPE, *LPCOLORPROFILETYPE;</code>




## -see-also




<a href="https://msdn.microsoft.com/b5cc965e-47b2-4309-8558-5208c7a2b587">COLORPROFILESUBTYPE</a>
 

 

