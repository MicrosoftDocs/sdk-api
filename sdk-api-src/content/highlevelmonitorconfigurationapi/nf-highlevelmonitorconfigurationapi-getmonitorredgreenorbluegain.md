---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorRedGreenOrBlueGain
title: GetMonitorRedGreenOrBlueGain function (highlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's red, green, or blue gain value.
helpviewer_keywords: ["GetMonitorRedGreenOrBlueGain","GetMonitorRedGreenOrBlueGain function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueGain","monitor.getmonitorredgreenorbluegain"]
old-location: monitor\getmonitorredgreenorbluegain.htm
tech.root: Monitor
ms.assetid: 058d70c4-a29c-4916-a4b9-911db5863363
ms.date: 12/05/2018
ms.keywords: GetMonitorRedGreenOrBlueGain, GetMonitorRedGreenOrBlueGain function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueGain, monitor.getmonitorredgreenorbluegain
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
 - GetMonitorRedGreenOrBlueGain
 - highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueGain
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
 - GetMonitorRedGreenOrBlueGain
---

# GetMonitorRedGreenOrBlueGain function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves a monitor's red, green, or blue gain value.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param gtGainType [in]

A member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_gain_type">MC_GAIN_TYPE</a> enumeration, specifying whether to retrieve the red, green, or blue gain value.

### -param pdwMinimumGain [out]

Receives the minimum red, green, or blue gain value.

### -param pdwCurrentGain [out]

Receives the current red, green, or blue gain value.

### -param pdwMaximumGain [out]

Receives the maximum red, green, or blue gain value.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Gain settings are generally used to adjust the monitor's white point.
      

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_RED_GREEN_BLUE_GAIN flag.
      

This function takes about 40 milliseconds to return.
      

The gain settings are continuous monitor settings. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive">GetMonitorRedGreenOrBlueDrive</a>



<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>