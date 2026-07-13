---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorCapabilities
title: GetMonitorCapabilities function (highlevelmonitorconfigurationapi.h)
description: Retrieves the configuration capabilities of a monitor. Call this function to find out which high-level monitor configuration functions are supported by the monitor.
helpviewer_keywords: ["GetMonitorCapabilities","GetMonitorCapabilities function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorCapabilities","monitor.getmonitorcapabilities"]
old-location: monitor\getmonitorcapabilities.htm
tech.root: Monitor
ms.assetid: 57cf0004-58cf-46d9-b5be-22edda2ce5a9
ms.date: 12/05/2018
ms.keywords: GetMonitorCapabilities, GetMonitorCapabilities function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorCapabilities, monitor.getmonitorcapabilities
req.header: highlevelmonitorconfigurationapi.h
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
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMonitorCapabilities
 - highlevelmonitorconfigurationapi/GetMonitorCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetMonitorCapabilities
---

# GetMonitorCapabilities function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves the configuration capabilities of a monitor. Call this function to find out which high-level monitor configuration functions are supported by the monitor.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param pdwMonitorCapabilities [out]

Receives a bitwise <b>OR</b> of capabilities flags. See Remarks.

### -param pdwSupportedColorTemperatures [out]

Receives a bitwise <b>OR</b> of color temperature flags. See Remarks.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The function fails if the monitor does not support DDC/CI.

## -remarks

The capabilities flags returned in <i>pdwMonitorCapabilities</i> specify which high-level monitor configuration functions are supported by the monitor. They also specify how certain functions behave. The following capabilities flags are defined.

<table>
<tr>
<th>Value</th>
<th>Description
            </th>
</tr>
<tr>
<td><b>MC_CAPS_BRIGHTNESS</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorbrightness">GetMonitorBrightness</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorbrightness">SetMonitorBrightness</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_COLOR_TEMPERATURE</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature">GetMonitorColorTemperature</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature">SetMonitorColorTemperature</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_CONTRAST</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcontrast">GetMonitorContrast</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcontrast">SetMonitorContrast</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_DEGAUSS</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-degaussmonitor">DegaussMonitor</a> function.</td>
</tr>
<tr>
<td><b>MC_CAPS_DISPLAY_AREA_POSITION</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition">GetMonitorDisplayAreaPosition</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition">SetMonitorDisplayAreaPosition</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_DISPLAY_AREA_SIZE</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize">GetMonitorDisplayAreaSize</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize">SetMonitorDisplayAreaSize</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_MONITOR_TECHNOLOGY_TYPE</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype">GetMonitorTechnologyType</a> function.</td>
</tr>
<tr>
<td><b>MC_CAPS_NONE</b></td>
<td>The monitor does not support any monitor settings.</td>
</tr>
<tr>
<td><b>MC_CAPS_RED_GREEN_BLUE_DRIVE</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive">GetMonitorRedGreenOrBlueDrive</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive">SetMonitorRedGreenOrBlueDrive</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_RED_GREEN_BLUE_GAIN</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain">GetMonitorRedGreenOrBlueGain</a> and <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain">SetMonitorRedGreenOrBlueGain</a> functions.</td>
</tr>
<tr>
<td><b>MC_CAPS_RESTORE_FACTORY_COLOR_DEFAULTS</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults">RestoreMonitorFactoryColorDefaults</a> function.</td>
</tr>
<tr>
<td><b>MC_CAPS_RESTORE_FACTORY_DEFAULTS</b></td>
<td>The monitor supports the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults">RestoreMonitorFactoryDefaults</a> function.</td>
</tr>
<tr>
<td><b>MC_RESTORE_FACTORY_DEFAULTS_ENABLES_MONITOR_SETTINGS</b></td>
<td>If this flag is present, calling the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults">RestoreMonitorFactoryDefaults</a> function enables all of the monitor settings used by the high-level monitor configuration functions. For more information, see the Remarks section in <b>RestoreMonitorFactoryDefaults</b>.</td>
</tr>
</table>
 

The color temperature flags returned in <i>pdwSupportedColorTemperatures</i> specify which color temperatures are supported by the monitor. The following color temperature flags are defined.

<table>
<tr>
<th>Value
            </th>
<th>Description
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

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
