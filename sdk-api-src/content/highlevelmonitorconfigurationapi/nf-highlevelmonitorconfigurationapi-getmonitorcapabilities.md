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

# GetMonitorCapabilities function


## -description



        Retrieves the configuration capabilities of a monitor. Call this function to find out which high-level monitor configuration functions are supported by the monitor.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pdwMonitorCapabilities [out]


            Receives a bitwise <b>OR</b> of capabilities flags. See Remarks.
          


### -param pdwSupportedColorTemperatures [out]


            Receives a bitwise <b>OR</b> of color temperature flags. See Remarks.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <b>GetLastError</b>.

The function fails if the monitor does not support DDC/CI.
          




## -remarks



The capabilities flags returned in <i>pdwMonitorCapabilities</i> specify which high-level monitor configuration functions are supported by the monitor. They also specify how certain functions behave. The following capabilities flags are defined.

<table>
<tr>
<th>
              Value</th>
<th>
              Description
            </th>
</tr>
<tr>
<td><b>MC_CAPS_BRIGHTNESS</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/eafdec51-067c-4b57-ac07-ca6237bcde14">GetMonitorBrightness</a> and <a href="https://msdn.microsoft.com/e7cf47f2-f833-4f34-89d2-3143ab57b561">SetMonitorBrightness</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_COLOR_TEMPERATURE</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/872aabcc-b274-454c-a08b-6c4c5aa83012">GetMonitorColorTemperature</a> and <a href="https://msdn.microsoft.com/a7f2753c-810f-41e5-9378-4072e8d4bc38">SetMonitorColorTemperature</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_CONTRAST</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/996d894d-3939-418f-b7d2-c0e9d667391e">GetMonitorContrast</a> and <a href="https://msdn.microsoft.com/7957702b-0ca2-4aaa-bae7-2518d2628f64">SetMonitorContrast</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_DEGAUSS</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/8f476ba3-24d2-456a-9335-873368993d71">DegaussMonitor</a> function.</td>
</tr>
<tr>
<td><b>MC_CAPS_DISPLAY_AREA_POSITION</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/d6dca744-634e-420f-a025-5be9d136969f">GetMonitorDisplayAreaPosition</a> and <a href="https://msdn.microsoft.com/ad7604e5-5ede-479b-881e-0a6060182e5b">SetMonitorDisplayAreaPosition</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_DISPLAY_AREA_SIZE</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/c27cbcf8-bb89-47c4-9f37-8b7a3d61c99f">GetMonitorDisplayAreaSize</a> and <a href="https://msdn.microsoft.com/0c3acb13-c5db-44ce-937d-b0b001a08062">SetMonitorDisplayAreaSize</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_MONITOR_TECHNOLOGY_TYPE</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/da3a5f64-2638-464b-973b-33cbe4cc64e7">GetMonitorTechnologyType</a> function.</td>
</tr>
<tr>
<td><b>MC_CAPS_NONE</b></td>
<td>The monitor does not support any monitor settings.</td>
</tr>
<tr>
<td><b>MC_CAPS_RED_GREEN_BLUE_DRIVE</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/4c590d1c-be28-401a-a0e9-dacf6b86a569">GetMonitorRedGreenOrBlueDrive</a> and <a href="https://msdn.microsoft.com/9d000d86-02f8-442f-954c-c039c9dcc0cd">SetMonitorRedGreenOrBlueDrive</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_RED_GREEN_BLUE_GAIN</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/058d70c4-a29c-4916-a4b9-911db5863363">GetMonitorRedGreenOrBlueGain</a> and <a href="https://msdn.microsoft.com/e8814478-1129-421e-999c-f59321db69b9">SetMonitorRedGreenOrBlueGain</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_RESTORE_FACTORY_COLOR_DEFAULTS</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/e5676134-ae4d-4db6-86fa-dbff0dd14a25">RestoreMonitorFactoryColorDefaults</a> function.</td>
</tr>
<tr>
<td><b>MC_CAPS_RESTORE_FACTORY_DEFAULTS</b></td>
<td>The monitor supports the <a href="https://msdn.microsoft.com/e7ce81c6-28a5-4371-8fc6-d13de33c2e80">RestoreMonitorFactoryDefaults</a> function.</td>
</tr>
<tr>
<td><b>MC_RESTORE_FACTORY_DEFAULTS_ENABLES_MONITOR_SETTINGS</b></td>
<td>If this flag is present, calling the <a href="https://msdn.microsoft.com/e7ce81c6-28a5-4371-8fc6-d13de33c2e80">RestoreMonitorFactoryDefaults</a> function enables all of the monitor settings used by the high-level monitor configuration functions. For more information, see the Remarks section in <b>RestoreMonitorFactoryDefaults</b>.</td>
</tr>
</table>
 

The color temperature flags returned in <i>pdwSupportedColorTemperatures</i> specify which color temperatures are supported by the monitor. The following color temperature flags are defined.

<table>
<tr>
<th>
              Value
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_NONE</b></td>
<td>No color temperatures are supported.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_4000K</b></td>
<td>The monitor supports 4,000 kelvins (K) color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_5000K</b></td>
<td>The monitor supports 5,000 K color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_6500K</b></td>
<td>The monitor supports 6,500 K color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_7500K</b></td>
<td>The monitor supports 7,500 K color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_8200K</b></td>
<td>The monitor supports 8,200 K color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_9300K</b></td>
<td>The monitor supports 9,300 K color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_10000K</b></td>
<td>The monitor supports 10,000 K color temperature.</td>
</tr>
<tr>
<td><b>MC_SUPPORTED_COLOR_TEMPERATURE_11500K</b></td>
<td>The monitor supports 11,500 K color temperature.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

