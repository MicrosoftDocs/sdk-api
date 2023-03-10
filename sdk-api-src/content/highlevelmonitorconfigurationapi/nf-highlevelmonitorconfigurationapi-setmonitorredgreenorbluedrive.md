---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorRedGreenOrBlueDrive
title: SetMonitorRedGreenOrBlueDrive function (highlevelmonitorconfigurationapi.h)
description: Sets a monitor's red, green, or blue drive value.
helpviewer_keywords: ["SetMonitorRedGreenOrBlueDrive","SetMonitorRedGreenOrBlueDrive function [Monitor Configuration]","highlevelmonitorconfigurationapi/SetMonitorRedGreenOrBlueDrive","monitor.setmonitorredgreenorbluedrive"]
old-location: monitor\setmonitorredgreenorbluedrive.htm
tech.root: Monitor
ms.assetid: 9d000d86-02f8-442f-954c-c039c9dcc0cd
ms.date: 12/05/2018
ms.keywords: SetMonitorRedGreenOrBlueDrive, SetMonitorRedGreenOrBlueDrive function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorRedGreenOrBlueDrive, monitor.setmonitorredgreenorbluedrive
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
 - SetMonitorRedGreenOrBlueDrive
 - highlevelmonitorconfigurationapi/SetMonitorRedGreenOrBlueDrive
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
 - SetMonitorRedGreenOrBlueDrive
---

# SetMonitorRedGreenOrBlueDrive function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Sets a monitor's red, green, or blue drive value.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param dtDriveType [in]

A member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_drive_type">MC_DRIVE_TYPE</a> enumeration, specifying whether to set the red, green, or blue drive value.

### -param dwNewDrive [in]

Red, green, or blue drive value. To get the monitor's minimum and maximum drive values, call <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive">GetMonitorRedGreenOrBlueDrive</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call GetLastError.

## -remarks

Drive settings are generally used to adjust the monitor's white point. <i>Drive</i> and <i>black level</i> are different names for the same monitor setting.
      

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_RED_GREEN_BLUE_DRIVE flag.
      

This function takes about 50 milliseconds to return.
      

Changing the drive settings can change the color temperature. To get the new color temperature, call <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature">GetMonitorColorTemperature</a>.
      

The drive settings are continuous monitor settings. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>