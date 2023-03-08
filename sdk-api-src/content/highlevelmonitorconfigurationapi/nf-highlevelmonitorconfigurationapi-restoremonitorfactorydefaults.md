---
UID: NF:highlevelmonitorconfigurationapi.RestoreMonitorFactoryDefaults
title: RestoreMonitorFactoryDefaults function (highlevelmonitorconfigurationapi.h)
description: Restores a monitor's settings to their factory defaults.
helpviewer_keywords: ["RestoreMonitorFactoryDefaults","RestoreMonitorFactoryDefaults function [Monitor Configuration]","highlevelmonitorconfigurationapi/RestoreMonitorFactoryDefaults","monitor.restoremonitorfactorydefaults"]
old-location: monitor\restoremonitorfactorydefaults.htm
tech.root: Monitor
ms.assetid: e7ce81c6-28a5-4371-8fc6-d13de33c2e80
ms.date: 12/05/2018
ms.keywords: RestoreMonitorFactoryDefaults, RestoreMonitorFactoryDefaults function [Monitor Configuration], highlevelmonitorconfigurationapi/RestoreMonitorFactoryDefaults, monitor.restoremonitorfactorydefaults
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
 - RestoreMonitorFactoryDefaults
 - highlevelmonitorconfigurationapi/RestoreMonitorFactoryDefaults
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
 - RestoreMonitorFactoryDefaults
---

# RestoreMonitorFactoryDefaults function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Restores a monitor's settings to their factory defaults.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function restores all of the settings that are supported by the high-level monitor configuration functions. It might also restore settings that are available only through the low-level functions and are not supported by the high-level functions. The current value of each setting is changed to its factory default. The exact settings that change, and the default values of those settings, depend on the manufacturer. This function can also change the range of supported values for some settings.
      

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_RESTORE_FACTORY_DEFAULTS flag.
      

This function takes about 5 seconds to return.
      

If <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> returns the MC_RESTORE_FACTORY_DEFAULTS_ENABLES_MONITOR_SETTINGS flag, this function also enables all of the monitor settings that are supported by the high-level functions. It is sometimes possible for an application to disable certain settings by calling the low-level functions. It is also possible for the user to disable certain settings by adjusting settings on the monitor's physical control panel. If that happens, the setting can only be re-enabled through the control panel or by calling <b>RestoreMonitorFactoryDefaults</b>. It is not possible to disable any settings by using the high-level functions.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>



<a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults">RestoreMonitorFactoryColorDefaults</a>