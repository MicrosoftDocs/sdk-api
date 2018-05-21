---
UID: NF:shellscalingapi.GetScaleFactorForDevice
title: GetScaleFactorForDevice function
author: windows-driver-content
description: Gets the preferred scale factor for a display device.
old-location: shell\getscalefactorfordevice.htm
old-project: shell
ms.assetid: 5F312914-03F6-42E0-80F9-761D854A81A3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetScaleFactorForDevice, GetScaleFactorForDevice function [Windows Shell], shell.getscalefactorfordevice, shellscalingapi/GetScaleFactorForDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shcore.dll
-	API-MS-Win-shcore-scaling-l1-1-0.dll
-	API-MS-Win-shcore-scaling-l1-1-1.dll
-	API-MS-Win-ShCore-Scaling-l1-1-2.dll
-	api-ms-win-shcore-scaling-l1.dll
api_name:
-	GetScaleFactorForDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Shcore.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# GetScaleFactorForDevice function


## -description


Gets the preferred scale factor for a display device.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="https://msdn.microsoft.com/2F214512-704D-41A2-86A6-1EF880CD3DB4">GetScaleFactorForMonitor</a> instead.</div><div> </div>

## -parameters




### -param deviceType [in]

Type: <b><a href="https://msdn.microsoft.com/C8964494-339B-4198-A544-3BBCCFEB9596">DISPLAY_DEVICE_TYPE</a></b>

The value that indicates the type of the display device.


## -returns



Type: <b><a href="https://msdn.microsoft.com/DB42E7D5-4E42-4b78-89F8-0B76320E2C5F">DEVICE_SCALE_FACTOR</a></b>

A value that indicates the scale factor that should be used with the specified <a href="https://msdn.microsoft.com/C8964494-339B-4198-A544-3BBCCFEB9596">DISPLAY_DEVICE_TYPE</a>.

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



The default <a href="https://msdn.microsoft.com/DB42E7D5-4E42-4b78-89F8-0B76320E2C5F">DEVICE_SCALE_FACTOR</a> is <a href="DEVICE_SCALE_FACTOR.htm">SCALE_100_PERCENT</a>.

Use the scale factor that is returned to scale point values for fonts and pixel values.




## -see-also




<a href="https://msdn.microsoft.com/2F214512-704D-41A2-86A6-1EF880CD3DB4">GetScaleFactorForMonitor</a>



<a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>



<a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a>
 

 

