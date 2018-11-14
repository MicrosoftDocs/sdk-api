---
UID: NF:highlevelmonitorconfigurationapi.SaveCurrentMonitorSettings
title: SaveCurrentMonitorSettings function
author: windows-sdk-content
description: Saves the current monitor settings to the display's nonvolatile storage.
old-location: monitor\savecurrentmonitorsettings.htm
tech.root: Monitor
ms.assetid: 933106f7-970e-466b-8f66-741e8ba39450
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SaveCurrentMonitorSettings, SaveCurrentMonitorSettings function [Monitor Configuration], highlevelmonitorconfigurationapi/SaveCurrentMonitorSettings, monitor.savecurrentmonitorsettings
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
 - SaveCurrentMonitorSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SaveCurrentMonitorSettings
: 
---

# SaveCurrentMonitorSettings function


## -description


Saves the current monitor settings to the display's nonvolatile storage.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



This function takes about 200 milliseconds to return.
      

This high-level function is identical to the low-level function <a href="https://msdn.microsoft.com/e5903e52-d04c-4ac3-9566-eb4f2559464b">SaveCurrentSettings</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

