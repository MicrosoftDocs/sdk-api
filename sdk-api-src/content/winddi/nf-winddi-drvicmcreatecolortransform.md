---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DrvIcmCreateColorTransform function


## -description


The <b>DrvIcmCreateColorTransform</b> function creates an ICM color transform.


## -parameters




### -param dhpdev [in]

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


### -param pLogColorSpace [in]

Pointer to a logical color space structure. The LOGCOLORSPACEW structure is defined in the Microsoft Windows SDK documentation. The driver should obtain source color space information from this structure when <i>pvSourceProfile</i> is <b>NULL</b>.


### -param pvSourceProfile [in, optional]

Pointer to the memory map of the source profile. This parameter can be <b>NULL</b>.


### -param cjSourceProfile [in]

Specifies the size, in bytes, of the source profile memory map. If <i>pvSourceProfile</i> is <b>NULL</b>, this parameter should be set to zero.


### -param pvDestProfile [in]

Pointer to the memory map of the destination profile.


### -param cjDestProfile [in]

Specifies the size, in bytes, of the destination profile memory map.


### -param pvTargetProfile [in, optional]

Pointer to the memory map of the target profile. This parameter can be <b>NULL</b>.


### -param cjTargetProfile [in]

Specifies the size, in bytes, of the target profile memory map. If <i>pvTargetProfile</i> is <b>NULL</b>, this parameter should be set to zero.


### -param dwReserved [in]

Reserved parameter that should be set to zero.


## -returns



<b>DrvIcmCreateColorTransform</b> returns a handle to the created transform upon success. Otherwise, it reports an error and returns <b>NULL</b>.




## -remarks



The driver creates a color transform from the profile data as follows:

<ul>
<li>
The driver should use the source profile that <i>pvSourceProfile</i> points to when it is not <b>NULL</b>. Otherwise, the driver should use the data in the structure to which <i>pLogColorSpace</i> points for source color space information.

</li>
<li>
When the driver receives a destination profile but no target profile, it should store the data required to transform colors from the specified source color space into the specified destination color space.

</li>
<li>
When the driver receives both destination and target profiles, it should store the data required to transform colors from the specified source color space into the specified target color space and from the target color space back to the destination color space. In this scenario, the driver's device is the destination device on which an image can be proofed. The driver must then be able to convert the color space of the proofing image into the target device's color space.

</li>
</ul>
Regardless of whether a target profile is specified, the driver's device is always the destination device.

The provided profiles adhere to version 2.10 of the ICC profile format. If the driver does not understand the specified format, it should fail the call.

The driver can safely access the entire memory map of each profile. The <i>pvSourceProfile</i>, <i>pvDestProfile</i>, and <i>pvTargetProfile</i> pointers are valid only during the scope of the call to <b>DrvIcmCreateTransform</b>.

Drivers that report ICM support should implement this function. A driver indicates support for ICM by setting the GCAPS_ICM flag in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556241">DrvIcmDeleteColorTransform</a>
 

 

