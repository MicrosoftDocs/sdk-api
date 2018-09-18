---
UID: NF:shellscalingapi.GetScaleFactorForMonitor
title: GetScaleFactorForMonitor function
author: windows-sdk-content
description: Gets the scale factor of a specific monitor. This function replaces GetScaleFactorForDevice.
old-location: shell\GetScaleFactorForMonitor.htm
tech.root: shell
ms.assetid: 2F214512-704D-41A2-86A6-1EF880CD3DB4
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetScaleFactorForMonitor, GetScaleFactorForMonitor function [Windows Shell], shell.GetScaleFactorForMonitor, shellscalingapi/GetScaleFactorForMonitor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - GetScaleFactorForMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetScaleFactorForMonitor function


## -description


Gets the scale factor of a specific monitor. This function replaces <a href="https://msdn.microsoft.com/5F312914-03F6-42E0-80F9-761D854A81A3">GetScaleFactorForDevice</a>.


## -parameters




### -param hMon [in]

The monitor's handle.


### -param pScale [out]

When this function returns successfully, this value points to one of the <a href="https://msdn.microsoft.com/DB42E7D5-4E42-4b78-89F8-0B76320E2C5F">DEVICE_SCALE_FACTOR</a> values that specify the scale factor of the specified monitor.
                        

If the function call fails, this value points to a valid scale factor so that apps can opt to continue on with incorrectly sized resources.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Your code needs to handle the <a href="https://msdn.microsoft.com/1eabd0b1-1f92-4576-b7fb-8af50fb04526">WM_WINDOWPOSCHANGED</a> message in addition to the scale change event registered through <a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>, because the app window can be moved between monitors. In response to the <b>WM_WINDOWPOSCHANGED</b> message, call <a href="https://msdn.microsoft.com/fe6505c9-b481-4fec-ae9d-995943234a3a">MonitorFromWindow</a>, followed by <b>GetScaleFactorForMonitor</b> to get the scale factor of the monitor which the app window is on. Your code can then react to any dots per inch (dpi) change by reloading assets and changing layout.




## -see-also




<a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>



<a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a>
 

 

