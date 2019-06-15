---
UID: NF:highlevelmonitorconfigurationapi.DegaussMonitor
title: DegaussMonitor function (highlevelmonitorconfigurationapi.h)
author: windows-sdk-content
description: Degausses a monitor.
old-location: monitor\degaussmonitor.htm
tech.root: Monitor
ms.assetid: 8f476ba3-24d2-456a-9335-873368993d71
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DegaussMonitor, DegaussMonitor function [Monitor Configuration], highlevelmonitorconfigurationapi/DegaussMonitor, monitor.degaussmonitor
ms.topic: function
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
 - DegaussMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DegaussMonitor function


## -description


Degausses a monitor. Degaussing improves a monitor's image quality and color fidelity by demagnetizing the monitor.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://docs.microsoft.com/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities">GetMonitorCapabilities</a> function returns the MC_CAPS_DEGAUSS flag. Degaussing is supported only by cathode ray tube (CRT) monitors.
      

This function takes about 50 milliseconds to return.
      

This function should not be called frequently, because calling it frequently will not noticeably improve the monitor's image quality or color fidelity.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

