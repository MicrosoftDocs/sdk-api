---
UID: NF:highlevelmonitorconfigurationapi.RestoreMonitorFactoryColorDefaults
title: RestoreMonitorFactoryColorDefaults function
author: windows-sdk-content
description: Restores a monitor's color settings to their factory defaults.
old-location: monitor\restoremonitorfactorycolordefaults.htm
old-project: Monitor
ms.assetid: e5676134-ae4d-4db6-86fa-dbff0dd14a25
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RestoreMonitorFactoryColorDefaults, RestoreMonitorFactoryColorDefaults function [Monitor Configuration], highlevelmonitorconfigurationapi/RestoreMonitorFactoryColorDefaults, monitor.restoremonitorfactorycolordefaults
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MC_SIZE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - RestoreMonitorFactoryColorDefaults
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# RestoreMonitorFactoryColorDefaults function


## -description



        Restores a monitor's color settings to their factory defaults.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


## -returns




            If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks




        This function potentially changes the current value of the monitor's brightness, contrast, color temperature, drive, and gain. The current value of each setting is changed to its factory default. The default settings depend on the manufacturer. This function can also change the range of supported values for each of these settings. The function does not enable any monitor settings that were disabled.
      


        If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_RESTORE_FACTORY_COLOR_DEFAULTS flag. This function takes about 5 seconds to return.
      


        This function might reset monitor settings that are not accessible through the high-level monitor configuration functions. Whether this occurs depends on the specific model of monitor.
      

The following settings are not affected by this function:

<ul>
<li>Display area size</li>
<li>Display area position</li>
<li>Capabilities flags</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>



<a href="https://msdn.microsoft.com/e7ce81c6-28a5-4371-8fc6-d13de33c2e80">RestoreMonitorFactoryDefaults</a>
 

 

