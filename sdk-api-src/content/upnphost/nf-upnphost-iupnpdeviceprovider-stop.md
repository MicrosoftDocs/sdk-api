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

# IUPnPDeviceProvider::Stop


## -description


The 
<b>Stop</b> method stops the device provider. This method is invoked by the device host before it unloads the device provider. This method is invoked when a service stops or the computer is shut down, and performs any cleanup processing required by the device provider.


## -parameters






## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/daaa8b55-bcef-4142-8f7b-e6f64e0ac258">IUPnPDeviceProvider</a>



<a href="https://msdn.microsoft.com/a76c7063-bad5-4f59-a5ca-8a8a4a79787e">IUPnPDeviceProvider::Start</a>
 

 

