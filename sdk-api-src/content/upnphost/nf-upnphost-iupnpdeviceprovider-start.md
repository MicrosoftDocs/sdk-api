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

# IUPnPDeviceProvider::Start


## -description


The 
<b>Start</b> method starts the device provider. The device host invokes this method after it loads the device provider This method performs any initialization required by the device provider.


## -parameters




### -param bstrInitString [in]

Identifies the initialization string specific to a device provider. This string is the same as the one passed to 
<a href="https://msdn.microsoft.com/40f91b29-b535-46e7-834f-97f1a46084f7">IUPnPRegistrar::RegisterDeviceProvider</a> at registration.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/daaa8b55-bcef-4142-8f7b-e6f64e0ac258">IUPnPDeviceProvider</a>



<a href="https://msdn.microsoft.com/c8e4cd95-a6dc-4bf9-921e-63fbac743028">IUPnPDeviceProvider::Stop</a>
 

 

