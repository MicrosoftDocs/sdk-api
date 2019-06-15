---
UID: NF:highlevelmonitorconfigurationapi.SaveCurrentMonitorSettings
title: SaveCurrentMonitorSettings function (highlevelmonitorconfigurationapi.h)
author: windows-sdk-content
description: Saves the current monitor settings to the display's nonvolatile storage.
old-location: monitor\savecurrentmonitorsettings.htm
tech.root: Monitor
ms.assetid: 933106f7-970e-466b-8f66-741e8ba39450
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SaveCurrentMonitorSettings, SaveCurrentMonitorSettings function [Monitor Configuration], highlevelmonitorconfigurationapi/SaveCurrentMonitorSettings, monitor.savecurrentmonitorsettings
ms.topic: function
f1_keywords: ["highlevelmonitorconfigurationapi/SaveCurrentMonitorSettings"]
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
ms.custom: 19H1
---

# SaveCurrentMonitorSettings function


## -description


Saves the current monitor settings to the display's nonvolatile storage.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



This function takes about 200 milliseconds to return.
      

This high-level function is identical to the low-level function <a href="https://docs.microsoft.com/windows/desktop/api/lowlevelmonitorconfigurationapi/nf-lowlevelmonitorconfigurationapi-savecurrentsettings">SaveCurrentSettings</a>.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

