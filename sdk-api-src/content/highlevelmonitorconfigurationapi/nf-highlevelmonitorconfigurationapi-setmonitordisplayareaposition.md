---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorDisplayAreaPosition
title: SetMonitorDisplayAreaPosition function (highlevelmonitorconfigurationapi.h)
description: Sets the horizontal or vertical position of a monitor's display area.
helpviewer_keywords: ["SetMonitorDisplayAreaPosition","SetMonitorDisplayAreaPosition function [Monitor Configuration]","highlevelmonitorconfigurationapi/SetMonitorDisplayAreaPosition","monitor.setmonitordisplayareaposition"]
old-location: monitor\setmonitordisplayareaposition.htm
tech.root: Monitor
ms.assetid: ad7604e5-5ede-479b-881e-0a6060182e5b
ms.date: 12/05/2018
ms.keywords: SetMonitorDisplayAreaPosition, SetMonitorDisplayAreaPosition function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorDisplayAreaPosition, monitor.setmonitordisplayareaposition
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
 - SetMonitorDisplayAreaPosition
 - highlevelmonitorconfigurationapi/SetMonitorDisplayAreaPosition
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
 - SetMonitorDisplayAreaPosition
---

# SetMonitorDisplayAreaPosition function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Sets the horizontal or vertical position of a monitor's display area.

Increasing the horizontal position moves the display area toward the right side of the screen; decreasing it moves the display area toward the left. Increasing the vertical position moves the display area toward the top of the screen; decreasing it moves the display area toward the bottom.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param ptPositionType [in]

A member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_position_type">MC_POSITION_TYPE</a> enumeration, specifying whether to set the horizontal position or the vertical position.

### -param dwNewPosition [in]

Horizontal or vertical position. To get the minimum and maximum position, call <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition">GetMonitorDisplayAreaPosition</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_POSITION flag.
      

This function takes about 50 milliseconds to return.
      

The horizontal and vertical position are continuous monitor settings. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>