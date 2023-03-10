---
UID: NF:winddi.DrvIcmSetDeviceGammaRamp
title: DrvIcmSetDeviceGammaRamp function (winddi.h)
description: The DrvIcmSetDeviceGammaRamp function sets the hardware gamma ramp of the specified display device.
helpviewer_keywords: ["DrvIcmSetDeviceGammaRamp","DrvIcmSetDeviceGammaRamp function [Display Devices]","ddifncs_4f81d949-51a0-4d83-b779-e9e950c2851d.xml","display.drvicmsetdevicegammaramp","winddi/DrvIcmSetDeviceGammaRamp"]
old-location: display\drvicmsetdevicegammaramp.htm
tech.root: display
ms.assetid: 0ea0c60c-fa12-4dd0-a6cc-45eacf4b73c0
ms.date: 12/05/2018
ms.keywords: DrvIcmSetDeviceGammaRamp, DrvIcmSetDeviceGammaRamp function [Display Devices], ddifncs_4f81d949-51a0-4d83-b779-e9e950c2851d.xml, display.drvicmsetdevicegammaramp, winddi/DrvIcmSetDeviceGammaRamp
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
 - DrvIcmSetDeviceGammaRamp
 - winddi/DrvIcmSetDeviceGammaRamp
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
 - DrvIcmSetDeviceGammaRamp
---

# DrvIcmSetDeviceGammaRamp function


## -description

The <b>DrvIcmSetDeviceGammaRamp</b> function sets the hardware <a href="/windows-hardware/drivers/">gamma ramp</a> of the specified display device.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a>. This identifies the physical device whose gamma ramp is to be set.

### -param iFormat

Specifies the data format of the buffer to which <i>lpRamp</i> points. This parameter is always IGRF_RGB_256WORDS.

### -param lpRamp

Pointer to the buffer containing the gamma ramp to be set on the device. The format of the data in this buffer is determined by <i>iFormat</i>.

When <i>iFormat</i> is IGRF_RGB_256WORDS, <i>lpRamp</i> points to a <a href="/windows/desktop/api/winddi/ns-winddi-gammaramp">GAMMARAMP</a> structure that defines the 256-entry ramps to be set for each of the red, blue, and green color channels. Each value is described using 16-bit precision. If the hardware has fewer bits of precision, it should downshift and use the most significant bits, without rounding.

## -returns

<b>DrvIcmSetDeviceGammaRamp</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.

## -remarks

Drivers for display devices with loadable hardware gamma ramps should implement this function.

<b>DrvIcmSetDeviceGammaRamp</b> should fail if it is called with any other value besides IGRF_RGB_256WORDS in <i>iFormat</i>.

The driver hooks this function by setting the GCAPS2_CHANGEGAMMARAMP flag in the <b>flGraphicsCaps2</b> field of the DEVINFO structure passed to <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>. If the driver is running in a palettized 8bpp mode, this capability is optional.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>