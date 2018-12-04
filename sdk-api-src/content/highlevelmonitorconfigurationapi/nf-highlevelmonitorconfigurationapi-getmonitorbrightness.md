---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorBrightness
title: GetMonitorBrightness function
author: windows-sdk-content
description: Retrieves a monitor's minimum, maximum, and current brightness settings.
old-location: monitor\getmonitorbrightness.htm
tech.root: Monitor
ms.assetid: eafdec51-067c-4b57-ac07-ca6237bcde14
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMonitorBrightness, GetMonitorBrightness function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorBrightness, monitor.getmonitorbrightness
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
 - GetMonitorBrightness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMonitorBrightness function


## -description


Retrieves a monitor's minimum, maximum, and current brightness settings.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pdwMinimumBrightness [out]

Receives the monitor's minimum brightness.
          


### -param pdwCurrentBrightness [out]

Receives the monitor's current brightness.
          


### -param pdwMaximumBrightness [out]

Receives the monitor's maximum brightness.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_BRIGHTNESS flag.
      

This function takes about 40 milliseconds to return.
      

The brightness setting is a continuous monitor setting. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

