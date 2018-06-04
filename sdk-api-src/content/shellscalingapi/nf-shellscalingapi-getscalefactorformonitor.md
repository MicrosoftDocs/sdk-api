---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

