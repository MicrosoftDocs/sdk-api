---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorContrast
title: GetMonitorContrast function (highlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's minimum, maximum, and current contrast settings.helpviewer_keywords: ["GetMonitorContrast","GetMonitorContrast function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorContrast","monitor.getmonitorcontrast"]
old-location: monitor\getmonitorcontrast.htm
tech.root: Monitor
ms.assetid: 996d894d-3939-418f-b7d2-c0e9d667391e
ms.date: 12/05/2018
ms.keywords: GetMonitorContrast, GetMonitorContrast function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorContrast, monitor.getmonitorcontrast
f1_keywords:
- highlevelmonitorconfigurationapi/GetMonitorContrast
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
- GetMonitorContrast
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMonitorContrast function


## -description


Retrieves a monitor's minimum, maximum, and current contrast settings.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pdwMinimumContrast [out]

Receives the monitor's minimum contrast.
          


### -param pdwCurrentContrast [out]

Receives the monitor's current contrast.
          


### -param pdwMaximumContrast [out]

Receives the monitor's maximum contrast.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://docs.microsoft.com/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_CONTRAST flag.
      

This function takes about 40 milliseconds to return.
      

The brightness setting is a continuous monitor setting. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

