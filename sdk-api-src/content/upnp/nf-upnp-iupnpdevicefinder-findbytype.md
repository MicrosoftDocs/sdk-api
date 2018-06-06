---
UID: NF:upnp.IUPnPDeviceFinder.FindByType
title: IUPnPDeviceFinder::FindByType
author: windows-sdk-content
description: The FindByType method searches synchronously for devices by device type or service type.
old-location: upnp\iupnpdevicefinder_findbytype.htm
old-project: UPnP
ms.assetid: 5fc28829-8802-457b-a1cf-c74834b6651c
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: FindByType, FindByType method [UPnP APIs], FindByType method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],FindByType method, IUPnPDeviceFinder.FindByType, IUPnPDeviceFinder::FindByType, _upnp_iupnpdevicefinder_findbytype, upnp.iupnpdevicefinder_findbytype, upnp/IUPnPDeviceFinder::FindByType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinder.FindByType
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceFinder::FindByType


## -description


The 
<b>FindByType</b> method searches synchronously for devices by device type or service type.


## -parameters




### -param bstrTypeURI [in]

Specifies the type URI for the device or service type for which to search.


### -param dwFlags [in]

Must be zero. This parameter is reserved for future use.


### -param pDevices [out]

Receives a reference to a collection of 
<a href="https://msdn.microsoft.com/237715dc-2b5a-45b4-b006-d31c0b4e89e3">IUPnPDevices</a> devices that were found.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



This method does not return until the search is complete. The search can take at least nine seconds, and possibly more. This method must not be called from a thread that processes user interface messages.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/88d4e004-7df8-45f4-b6ec-9dcf3f0ccfeb">IUPnPDeviceFinder::FindByUDN</a>



<a href="https://msdn.microsoft.com/237715dc-2b5a-45b4-b006-d31c0b4e89e3">IUPnPDevices</a>
 

 

