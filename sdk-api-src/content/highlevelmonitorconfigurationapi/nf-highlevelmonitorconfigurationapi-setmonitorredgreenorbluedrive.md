---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorRedGreenOrBlueDrive
title: SetMonitorRedGreenOrBlueDrive function (highlevelmonitorconfigurationapi.h)
author: windows-sdk-content
description: Sets a monitor's red, green, or blue drive value.
old-location: monitor\setmonitorredgreenorbluedrive.htm
tech.root: Monitor
ms.assetid: 9d000d86-02f8-442f-954c-c039c9dcc0cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetMonitorRedGreenOrBlueDrive, SetMonitorRedGreenOrBlueDrive function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorRedGreenOrBlueDrive, monitor.setmonitorredgreenorbluedrive
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
 - SetMonitorRedGreenOrBlueDrive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetMonitorRedGreenOrBlueDrive function


## -description


Sets a monitor's red, green, or blue drive value.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param dtDriveType [in]

A member of the <a href="https://msdn.microsoft.com/en-us/library/Dd692956(v=VS.85).aspx">MC_DRIVE_TYPE</a> enumeration, specifying whether to set the red, green, or blue drive value.
          


### -param dwNewDrive [in]

Red, green, or blue drive value. To get the monitor's minimum and maximum drive values, call <a href="https://msdn.microsoft.com/4c590d1c-be28-401a-a0e9-dacf6b86a569">GetMonitorRedGreenOrBlueDrive</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call GetLastError.




## -remarks



Drive settings are generally used to adjust the monitor's white point. <i>Drive</i> and <i>black level</i> are different names for the same monitor setting.
      

If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_RED_GREEN_BLUE_DRIVE flag.
      

This function takes about 50 milliseconds to return.
      

Changing the drive settings can change the color temperature. To get the new color temperature, call <a href="https://msdn.microsoft.com/872aabcc-b274-454c-a08b-6c4c5aa83012">GetMonitorColorTemperature</a>.
      

The drive settings are continuous monitor settings. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

