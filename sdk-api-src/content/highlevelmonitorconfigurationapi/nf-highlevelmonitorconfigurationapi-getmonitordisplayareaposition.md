---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorDisplayAreaPosition
title: GetMonitorDisplayAreaPosition function (highlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's minimum, maximum, and current horizontal or vertical position.
helpviewer_keywords: ["GetMonitorDisplayAreaPosition","GetMonitorDisplayAreaPosition function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorDisplayAreaPosition","monitor.getmonitordisplayareaposition"]
old-location: monitor\getmonitordisplayareaposition.htm
tech.root: Monitor
ms.assetid: d6dca744-634e-420f-a025-5be9d136969f
ms.date: 12/05/2018
ms.keywords: GetMonitorDisplayAreaPosition, GetMonitorDisplayAreaPosition function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorDisplayAreaPosition, monitor.getmonitordisplayareaposition
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
 - GetMonitorDisplayAreaPosition
 - highlevelmonitorconfigurationapi/GetMonitorDisplayAreaPosition
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
 - GetMonitorDisplayAreaPosition
---

# GetMonitorDisplayAreaPosition function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves a monitor's minimum, maximum, and current horizontal or vertical position.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param ptPositionType [in]

A member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_position_type">MC_POSITION_TYPE</a> enumeration, specifying whether to retrieve the horizontal position or the vertical position.

### -param pdwMinimumPosition [out]

Receives the minimum horizontal or vertical position.

### -param pdwCurrentPosition [out]

Receives the current horizontal or vertical position.

### -param pdwMaximumPosition [out]

Receives the maximum horizontal or vertical position.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_POSITION flag.
      

This function takes about 40 milliseconds to return.
      

The horizontal and vertical position are continuous monitor settings. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>