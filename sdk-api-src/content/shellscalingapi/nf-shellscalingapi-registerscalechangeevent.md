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

# RegisterScaleChangeEvent function


## -description


Registers for an event that is triggered when the scale has possibly changed. This function replaces <a href="https://msdn.microsoft.com/79FB0A54-EBF0-4aab-B631-B4D3EA54D20B">RegisterScaleChangeNotifications</a>.


## -parameters




### -param hEvent [in]

Handle of the event to register for scale change notifications.


### -param pdwCookie [out]

When this function returns successfully, this value receives the address of a pointer to a cookie that can be used later to unregister for the scale change notifications through <a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a>.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The event is raised whenever something that can affect scale changes, but just because the scale can be affected doesn't mean that it has been. Callers can cache the scale factor to verify that the monitor's scale actually has changed. The event handle will be duplicated, so callers can close their handle at any time.




## -see-also




<a href="https://msdn.microsoft.com/2F214512-704D-41A2-86A6-1EF880CD3DB4">GetScaleFactorForMonitor</a>



<a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a>
 

 

