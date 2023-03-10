---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorDisplayAreaSize
title: SetMonitorDisplayAreaSize function (highlevelmonitorconfigurationapi.h)
description: Sets the width or height of a monitor's display area.
helpviewer_keywords: ["SetMonitorDisplayAreaSize","SetMonitorDisplayAreaSize function [Monitor Configuration]","highlevelmonitorconfigurationapi/SetMonitorDisplayAreaSize","monitor.setmonitordisplayareasize"]
old-location: monitor\setmonitordisplayareasize.htm
tech.root: Monitor
ms.assetid: 0c3acb13-c5db-44ce-937d-b0b001a08062
ms.date: 12/05/2018
ms.keywords: SetMonitorDisplayAreaSize, SetMonitorDisplayAreaSize function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorDisplayAreaSize, monitor.setmonitordisplayareasize
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
 - SetMonitorDisplayAreaSize
 - highlevelmonitorconfigurationapi/SetMonitorDisplayAreaSize
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
 - SetMonitorDisplayAreaSize
---

# SetMonitorDisplayAreaSize function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Sets the width or height of a monitor's display area.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param stSizeType [in]

A member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_size_type">MC_SIZE_TYPE</a> enumeration, specifying whether to set the width or the height.

### -param dwNewDisplayAreaWidthOrHeight [in]

Display area width or height. To get the minimum and maximum width and height, call <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize">GetMonitorDisplayAreaSize</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is supported, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_SIZE flag.
      

This function takes about 50 milliseconds to return.
      

The width and height settings are continuous monitor settings. For more information, see <a href="/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>