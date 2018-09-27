---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorColorTemperature
title: GetMonitorColorTemperature function
author: windows-sdk-content
description: Retrieves a monitor's current color temperature.
old-location: monitor\getmonitorcolortemperature.htm
tech.root: Monitor
ms.assetid: 872aabcc-b274-454c-a08b-6c4c5aa83012
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetMonitorColorTemperature, GetMonitorColorTemperature function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorColorTemperature, monitor.getmonitorcolortemperature
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GetMonitorColorTemperature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMonitorColorTemperature function


## -description


Retrieves a monitor's current color temperature.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pctCurrentColorTemperature [out]

Receives the monitor's current color temperature, specified as a member of the <a href="https://msdn.microsoft.com/890d1d84-6a7d-457b-8136-230be4c79e78">MC_COLOR_TEMPERATURE</a> enumeration.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_COLOR_TEMPERATURE flag.
      

This function takes between 0 and 80 milliseconds to return.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

