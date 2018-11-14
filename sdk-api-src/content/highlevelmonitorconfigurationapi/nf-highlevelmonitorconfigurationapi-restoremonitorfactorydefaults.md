---
UID: NF:highlevelmonitorconfigurationapi.RestoreMonitorFactoryDefaults
title: RestoreMonitorFactoryDefaults function
author: windows-sdk-content
description: Restores a monitor's settings to their factory defaults.
old-location: monitor\restoremonitorfactorydefaults.htm
tech.root: Monitor
ms.assetid: e7ce81c6-28a5-4371-8fc6-d13de33c2e80
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RestoreMonitorFactoryDefaults, RestoreMonitorFactoryDefaults function [Monitor Configuration], highlevelmonitorconfigurationapi/RestoreMonitorFactoryDefaults, monitor.restoremonitorfactorydefaults
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
 - RestoreMonitorFactoryDefaults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RestoreMonitorFactoryDefaults
: 
---

# RestoreMonitorFactoryDefaults function


## -description


Restores a monitor's settings to their factory defaults.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



This function restores all of the settings that are supported by the high-level monitor configuration functions. It might also restore settings that are available only through the low-level functions and are not supported by the high-level functions. The current value of each setting is changed to its factory default. The exact settings that change, and the default values of those settings, depend on the manufacturer. This function can also change the range of supported values for some settings.
      

If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_RESTORE_FACTORY_DEFAULTS flag.
      

This function takes about 5 seconds to return.
      

If <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> returns the MC_RESTORE_FACTORY_DEFAULTS_ENABLES_MONITOR_SETTINGS flag, this function also enables all of the monitor settings that are supported by the high-level functions. It is sometimes possible for an application to disable certain settings by calling the low-level functions. It is also possible for the user to disable certain settings by adjusting settings on the monitor's physical control panel. If that happens, the setting can only be re-enabled through the control panel or by calling <b>RestoreMonitorFactoryDefaults</b>. It is not possible to disable any settings by using the high-level functions.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>



<a href="https://msdn.microsoft.com/e5676134-ae4d-4db6-86fa-dbff0dd14a25">RestoreMonitorFactoryColorDefaults</a>
 

 

