---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorColorTemperature
title: GetMonitorColorTemperature function (highlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's current color temperature.
helpviewer_keywords: ["GetMonitorColorTemperature","GetMonitorColorTemperature function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorColorTemperature","monitor.getmonitorcolortemperature"]
old-location: monitor\getmonitorcolortemperature.htm
tech.root: Monitor
ms.assetid: 872aabcc-b274-454c-a08b-6c4c5aa83012
ms.date: 12/05/2018
ms.keywords: GetMonitorColorTemperature, GetMonitorColorTemperature function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorColorTemperature, monitor.getmonitorcolortemperature
f1_keywords:
- highlevelmonitorconfigurationapi/GetMonitorColorTemperature
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- dxva2.dll
api_name:
- GetMonitorColorTemperature
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMonitorColorTemperature function


## -description


Retrieves a monitor's current color temperature.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pctCurrentColorTemperature [out]

Receives the monitor's current color temperature, specified as a member of the <a href="/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_color_temperature">MC_COLOR_TEMPERATURE</a> enumeration.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://docs.microsoft.com/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_COLOR_TEMPERATURE flag.
      

This function takes between 0 and 80 milliseconds to return.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

