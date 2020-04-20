---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorDisplayAreaSize
title: GetMonitorDisplayAreaSize function (highlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's minimum, maximum, and current width or height.helpviewer_keywords: ["GetMonitorDisplayAreaSize","GetMonitorDisplayAreaSize function [Monitor Configuration]","highlevelmonitorconfigurationapi/GetMonitorDisplayAreaSize","monitor.getmonitordisplayareasize"]
old-location: monitor\getmonitordisplayareasize.htm
tech.root: Monitor
ms.assetid: c27cbcf8-bb89-47c4-9f37-8b7a3d61c99f
ms.date: 12/05/2018
ms.keywords: GetMonitorDisplayAreaSize, GetMonitorDisplayAreaSize function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorDisplayAreaSize, monitor.getmonitordisplayareasize
f1_keywords:
- highlevelmonitorconfigurationapi/GetMonitorDisplayAreaSize
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
- GetMonitorDisplayAreaSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMonitorDisplayAreaSize function


## -description


Retrieves a monitor's minimum, maximum, and current width or height.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param stSizeType [in]

A member of the <a href="https://docs.microsoft.com/windows/win32/api/highlevelmonitorconfigurationapi/ne-highlevelmonitorconfigurationapi-mc_size_type">MC_SIZE_TYPE</a> enumeration, specifying whether to retrieve the width or the height.
          


### -param pdwMinimumWidthOrHeight [out]

Receives the minimum width or height.
          


### -param pdwCurrentWidthOrHeight [out]

Receives the current width or height.
          


### -param pdwMaximumWidthOrHeight [out]

Receives the maximum width or height.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://docs.microsoft.com/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_SIZE flag.
      

This function takes about 40 milliseconds to return.
      

The width and height settings are continuous monitor settings. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Monitor/using-the-high-level-monitor-configuration-functions">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

