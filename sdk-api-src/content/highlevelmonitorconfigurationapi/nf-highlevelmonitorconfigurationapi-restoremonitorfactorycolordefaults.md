---
UID: NF:highlevelmonitorconfigurationapi.RestoreMonitorFactoryColorDefaults
title: RestoreMonitorFactoryColorDefaults function (highlevelmonitorconfigurationapi.h)
description: Restores a monitor's color settings to their factory defaults.
helpviewer_keywords: ["RestoreMonitorFactoryColorDefaults","RestoreMonitorFactoryColorDefaults function [Monitor Configuration]","highlevelmonitorconfigurationapi/RestoreMonitorFactoryColorDefaults","monitor.restoremonitorfactorycolordefaults"]
old-location: monitor\restoremonitorfactorycolordefaults.htm
tech.root: Monitor
ms.assetid: e5676134-ae4d-4db6-86fa-dbff0dd14a25
ms.date: 12/05/2018
ms.keywords: RestoreMonitorFactoryColorDefaults, RestoreMonitorFactoryColorDefaults function [Monitor Configuration], highlevelmonitorconfigurationapi/RestoreMonitorFactoryColorDefaults, monitor.restoremonitorfactorycolordefaults
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
 - RestoreMonitorFactoryColorDefaults
 - highlevelmonitorconfigurationapi/RestoreMonitorFactoryColorDefaults
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
 - RestoreMonitorFactoryColorDefaults
---

# RestoreMonitorFactoryColorDefaults function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Restores a monitor's color settings to their factory defaults.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function potentially changes the current value of the monitor's brightness, contrast, color temperature, drive, and gain. The current value of each setting is changed to its factory default. The default settings depend on the manufacturer. This function can also change the range of supported values for each of these settings. The function does not enable any monitor settings that were disabled.
      

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_RESTORE_FACTORY_COLOR_DEFAULTS flag. This function takes about 5 seconds to return.
      

This function might reset monitor settings that are not accessible through the high-level monitor configuration functions. Whether this occurs depends on the specific model of monitor.
      

The following settings are not affected by this function:

<ul>
<li>Display area size</li>
<li>Display area position</li>
<li>Capabilities flags</li>
</ul>

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>



<a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults">RestoreMonitorFactoryDefaults</a>