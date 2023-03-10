---
UID: NF:winddi.DrvIcmCreateColorTransform
title: DrvIcmCreateColorTransform function (winddi.h)
description: The DrvIcmCreateColorTransform function creates an ICM color transform.
helpviewer_keywords: ["DrvIcmCreateColorTransform","DrvIcmCreateColorTransform function [Display Devices]","ddifncs_eec39816-8aa5-44a8-8fed-b800db94d315.xml","display.drvicmcreatecolortransform","winddi/DrvIcmCreateColorTransform"]
old-location: display\drvicmcreatecolortransform.htm
tech.root: display
ms.assetid: a4fda665-ba26-4799-820d-c4d82a58d6fd
ms.date: 12/05/2018
ms.keywords: DrvIcmCreateColorTransform, DrvIcmCreateColorTransform function [Display Devices], ddifncs_eec39816-8aa5-44a8-8fed-b800db94d315.xml, display.drvicmcreatecolortransform, winddi/DrvIcmCreateColorTransform
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvIcmCreateColorTransform
 - winddi/DrvIcmCreateColorTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvIcmCreateColorTransform
---

# DrvIcmCreateColorTransform function


## -description

The <b>DrvIcmCreateColorTransform</b> function creates an ICM color transform.

## -parameters

### -param dhpdev [in]

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a>.

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

Drivers that report ICM support should implement this function. A driver indicates support for ICM by setting the GCAPS_ICM flag in the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvicmdeletecolortransform">DrvIcmDeleteColorTransform</a>