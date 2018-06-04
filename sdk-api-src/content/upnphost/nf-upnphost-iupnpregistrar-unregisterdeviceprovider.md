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

# IUPnPRegistrar::UnregisterDeviceProvider


## -description


The 
<b>UnregisterDeviceProvider</b> method permanently unregisters and unloads the device provider from the device host. The 
<a href="https://msdn.microsoft.com/c8e4cd95-a6dc-4bf9-921e-63fbac743028">IUPnPDeviceProvider::Stop</a> method is invoked.


## -parameters




### -param bstrProviderName [in]

Specifies the provider name. Use the same name that was used in the call to 
<a href="https://msdn.microsoft.com/40f91b29-b535-46e7-834f-97f1a46084f7">RegisterDeviceProvider</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/c851e102-4f03-4a21-9e62-9b5c60a728f3">IUPnPRegistrar</a>
 

 

