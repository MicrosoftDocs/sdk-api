---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorBrightness
title: SetMonitorBrightness function (highlevelmonitorconfigurationapi.h)
description: Sets a monitor's brightness value.
helpviewer_keywords: ["SetMonitorBrightness","SetMonitorBrightness function [Monitor Configuration]","highlevelmonitorconfigurationapi/SetMonitorBrightness","monitor.setmonitorbrightness"]
old-location: monitor\setmonitorbrightness.htm
tech.root: Monitor
ms.assetid: e7cf47f2-f833-4f34-89d2-3143ab57b561
ms.date: 12/05/2018
ms.keywords: SetMonitorBrightness, SetMonitorBrightness function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorBrightness, monitor.setmonitorbrightness
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
 - SetMonitorBrightness
 - highlevelmonitorconfigurationapi/SetMonitorBrightness
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
 - SetMonitorBrightness
---

# SetMonitorBrightness function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Sets a monitor's brightness value. Increasing the brightness value makes the display on the monitor brighter, and decreasing it makes the display dimmer.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param dwNewBrightness [in]

Brightness value. To get the monitor's minimum and maximum brightness values, call <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorbrightness">GetMonitorBrightness</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_BRIGHTNESS flag.
      

This function takes about 50 milliseconds to return.
      

The brightness setting is a continuous monitor setting. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>