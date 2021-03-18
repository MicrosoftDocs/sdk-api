---
UID: NF:wingdi.SetDeviceGammaRamp
title: SetDeviceGammaRamp function (wingdi.h)
description: The SetDeviceGammaRamp function sets the gamma ramp on direct color display boards having drivers that support downloadable gamma ramps in hardware.
helpviewer_keywords: ["SetDeviceGammaRamp","SetDeviceGammaRamp function [Windows Color System]","_color_SetDeviceGammaRamp","wcs.setdevicegammaramp","wingdi/SetDeviceGammaRamp"]
old-location: wcs\setdevicegammaramp.htm
tech.root: WCS
ms.assetid: 8e4cc9a4-f292-47a1-a12a-43a479326ca7
ms.date: 12/05/2018
ms.keywords: SetDeviceGammaRamp, SetDeviceGammaRamp function [Windows Color System], _color_SetDeviceGammaRamp, wcs.setdevicegammaramp, wingdi/SetDeviceGammaRamp
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDeviceGammaRamp
 - wingdi/SetDeviceGammaRamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-wcs-l1-1-0.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetDeviceGammaRamp
---

## -description

The <b>SetDeviceGammaRamp</b> function sets the [gamma ramp](/windows/win32/wcs/g) on direct color display boards having drivers that support downloadable gamma ramps in hardware.

> [!IMPORTANT]
> We strongly recommend that you don't use this API. Use of this API is subject to major limitations:
>
> * **SetDeviceGammaRamp** implements heuristics to check whether a provided ramp will result in an unreadable screen. If a ramp violates those heuristics, then the function fails silently (that is, it returns **TRUE**, but it doesn't set your ramp). For that reason, you can't expect to use this function to set *just any arbitrary* gamma ramp. In particular, the heuristics prevent ramps that would result in nearly all pixels approaching a single value (such as fullscreen black/white) as this may prevent a user from recovering the screen.
>
> * Because of the function's global nature, any other application on the system could, at any time, overwrite any ramp that you've set. In some cases the operating system itself may reserve the use of this function, causing any existing ramp to be overwritten. The gamma ramp is also reset on most display events (connecting/disconnecting a monitor, resolution changes, etc.). So you can't be certain that any ramp you set is in effect.
>
> * This API has undefined behavior in HDR modes.
>
> * This API has undefined interaction with both built-in and third-party color calibration solutions.
>
> For color calibration, we recommend that you create an International Color Consortium (ICC) profile, and let the OS apply the profile. For advanced original equipment manufacturer (OEM) scenarios, there's a device driver model that you can use to customize color calibration more directly. See the [Windows Color System](/windows/win32/wcs/windows-color-system) for information on managing color profiles.
>
> For blue light filtering, Windows now provides built-in support called [**Night Light**](https://support.microsoft.com/help/4027563/windows-10-set-your-display-for-night-time). We recommend directing users to this feature.
>
> For color adaptation (for example, adjusting color calibration based on ambient light sensors), Windows now provides built-in support, which we recommend for use by OEMs.
>
> For custom filter effects, there are a variety of built-in accessibility [color filters](https://support.microsoft.com/help/4344736/windows-10-use-color-filters) to help with a range of cases.

## -parameters

### -param hdc

Specifies the device context of the direct color display board in question.

### -param lpRamp

Pointer to a buffer containing the gamma ramp to be set. The gamma ramp is specified in three arrays of 256 <b>WORD</b> elements each, which contain the mapping between RGB values in the frame buffer and digital-analog-converter (<i>DAC</i> ) values. The sequence of the arrays is red, green, blue. The RGB values must be stored in the most significant bits of each WORD to increase DAC independence.

## -returns

If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.

## -remarks

Direct color display modes do not use color lookup tables and are usually 16, 24, or 32 bit. Not all direct color video boards support loadable gamma ramps. <b>SetDeviceGammaRamp</b> succeeds only for devices with drivers that support downloadable gamma ramps in hardware.

> [!NOTE]
> This API can take a non-trivial amount of time to execute. It may take as long as 200ms to return on some hardware.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)