---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorRedGreenOrBlueDrive
title: GetMonitorRedGreenOrBlueDrive function (highlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's red, green, or blue drive value.
helpviewer_keywords: ["GetMonitorRedGreenOrBlueDrive","GetMonitorRedGreenOrBlueDrive function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueDrive","monitor.getmonitorredgreenorbluedrive"]
old-location: monitor\getmonitorredgreenorbluedrive.htm
tech.root: Monitor
ms.assetid: 4c590d1c-be28-401a-a0e9-dacf6b86a569
ms.date: 12/05/2018
ms.keywords: GetMonitorRedGreenOrBlueDrive, GetMonitorRedGreenOrBlueDrive function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueDrive, monitor.getmonitorredgreenorbluedrive
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
 - GetMonitorRedGreenOrBlueDrive
 - highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueDrive
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
 - GetMonitorRedGreenOrBlueDrive
---

# GetMonitorRedGreenOrBlueDrive function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves a monitor's red, green, or blue drive value.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param dtDriveType [in]

A member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_drive_type">MC_DRIVE_TYPE</a> enumeration, specifying whether to retrieve the red, green, or blue drive value.

### -param pdwMinimumDrive [out]

Receives the minimum red, green, or blue drive value.

### -param pdwCurrentDrive [out]

Receives the current red, green, or blue drive value.

### -param pdwMaximumDrive [out]

Receives the maximum red, green, or blue drive value.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Drive settings are generally used to adjust the monitor's white point. <i>Drive</i> and <i>black level</i> are different names for the same monitor setting. If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_RED_GREEN_BLUE_DRIVE flag.
      

This function takes about 40 milliseconds to return.
      

The drive settings are continuous monitor settings. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>