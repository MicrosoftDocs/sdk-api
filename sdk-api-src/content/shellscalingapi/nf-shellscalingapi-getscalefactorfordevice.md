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
 

 

