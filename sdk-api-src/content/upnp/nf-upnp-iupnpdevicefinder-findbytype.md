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
 

 

