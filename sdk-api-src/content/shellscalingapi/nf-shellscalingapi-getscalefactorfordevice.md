---
UID: NF:shellscalingapi.GetScaleFactorForDevice
title: GetScaleFactorForDevice function (shellscalingapi.h)
description: Gets the preferred scale factor for a display device.
helpviewer_keywords: ["GetScaleFactorForDevice","GetScaleFactorForDevice function [Windows Shell]","shell.getscalefactorfordevice","shellscalingapi/GetScaleFactorForDevice"]
old-location: shell\getscalefactorfordevice.htm
tech.root: shell
ms.assetid: 5F312914-03F6-42E0-80F9-761D854A81A3
ms.date: 12/05/2018
ms.keywords: GetScaleFactorForDevice, GetScaleFactorForDevice function [Windows Shell], shell.getscalefactorfordevice, shellscalingapi/GetScaleFactorForDevice
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.Lib
req.dll: Shcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetScaleFactorForDevice
 - shellscalingapi/GetScaleFactorForDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-0.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - GetScaleFactorForDevice
---

# GetScaleFactorForDevice function


## -description

Gets the preferred scale factor for a display device.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor">GetScaleFactorForMonitor</a> instead.</div><div> </div>

## -parameters

### -param deviceType [in]

Type: <b><a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-display_device_type">DISPLAY_DEVICE_TYPE</a></b>

The value that indicates the type of the display device.

## -returns

Type: <b><a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">DEVICE_SCALE_FACTOR</a></b>

A value that indicates the scale factor that should be used with the specified <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-display_device_type">DISPLAY_DEVICE_TYPE</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCALE_100_PERCENT</b></dt>
<dt>100</dt>
</dl>
</td>
<td width="60%">
Use a scale factor of 1x.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCALE_140_PERCENT</b></dt>
<dt>140</dt>
</dl>
</td>
<td width="60%">
Use a scale factor of 1.4x.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCALE_180_PERCENT</b></dt>
<dt>180</dt>
</dl>
</td>
<td width="60%">
Use a scale factor of 1.8x.

</td>
</tr>
</table>

## -remarks

The default <a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">DEVICE_SCALE_FACTOR</a> is <a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">SCALE_100_PERCENT</a>.

Use the scale factor that is returned to scale point values for fonts and pixel values.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor">GetScaleFactorForMonitor</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a>