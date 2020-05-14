---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorBrightness
title: SetMonitorBrightness function (highlevelmonitorconfigurationapi.h)
description: Sets a monitor's brightness value.helpviewer_keywords: ["SetMonitorBrightness","SetMonitorBrightness function [Monitor Configuration]","highlevelmonitorconfigurationapi/SetMonitorBrightness","monitor.setmonitorbrightness"]
old-location: monitor\setmonitorbrightness.htm
tech.root: Monitor
ms.assetid: e7cf47f2-f833-4f34-89d2-3143ab57b561
ms.date: 12/05/2018
ms.keywords: SetMonitorBrightness, SetMonitorBrightness function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorBrightness, monitor.setmonitorbrightness
f1_keywords:
- highlevelmonitorconfigurationapi/SetMonitorBrightness
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
- SetMonitorBrightness
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetMonitorBrightness function


## -description


Sets a monitor's brightness value. Increasing the brightness value makes the display on the monitor brighter, and decreasing it makes the display dimmer.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param dwNewBrightness [in]

Brightness value. To get the monitor's minimum and maximum brightness values, call <a href="https://docs.microsoft.com/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorbrightness">GetMonitorBrightness</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://docs.microsoft.com/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_BRIGHTNESS flag.
      

This function takes about 50 milliseconds to return.
      

The brightness setting is a continuous monitor setting. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

