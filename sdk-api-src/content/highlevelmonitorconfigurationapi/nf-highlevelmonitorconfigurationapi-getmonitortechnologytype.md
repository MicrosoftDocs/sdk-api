---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorTechnologyType
title: GetMonitorTechnologyType function (highlevelmonitorconfigurationapi.h)
description: Retrieves the type of technology used by a monitor.
helpviewer_keywords: ["GetMonitorTechnologyType","GetMonitorTechnologyType function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorTechnologyType","monitor.getmonitortechnologytype"]
old-location: monitor\getmonitortechnologytype.htm
tech.root: Monitor
ms.assetid: da3a5f64-2638-464b-973b-33cbe4cc64e7
ms.date: 12/05/2018
ms.keywords: GetMonitorTechnologyType, GetMonitorTechnologyType function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorTechnologyType, monitor.getmonitortechnologytype
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
 - GetMonitorTechnologyType
 - highlevelmonitorconfigurationapi/GetMonitorTechnologyType
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
 - GetMonitorTechnologyType
---

# GetMonitorTechnologyType function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves the type of technology used by a monitor.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param pdtyDisplayTechnologyType [out]

Receives the technology type, specified as a member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_display_technology_type">MC_DISPLAY_TECHNOLOGY_TYPE</a> enumeration.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function does not support every display technology. If a monitor uses a display technology that is supported by this function, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_TECHNOLOGY_TYPE flag. If that flag is absent, the <b>GetMonitorTechnologyType</b> function fails.
      

Some monitor technologies do not support certain monitor configuration functions. For example, the <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-degaussmonitor">DegaussMonitor</a> function is supported only for cathode ray tube (CRT) monitors. To find out whether a specific function is supported, call <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>