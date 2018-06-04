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

# IUPnPDeviceFinder::FindByUDN


## -description


The 
<b>FindByUDN</b> method searches synchronously for a device by its unique device name (UDN).


## -parameters




### -param bstrUDN [in]

Specifies the UDN for which to search. This value is case sensitive, and should be provided as  lower-case (e.g. uuid:e8f85dfd-ff...).


### -param pDevice [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that contains the requested device. Receives <b>NULL</b> if the specified device is not found.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns S_FALSE.




## -remarks



This method returns as soon as a device that matches the specified UDN is found. If no device is found, the method takes at least nine seconds to return, and possibly longer.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/5fc28829-8802-457b-a1cf-c74834b6651c">IUPnPDeviceFinder::FindByType</a>



<a href="https://msdn.microsoft.com/237715dc-2b5a-45b4-b006-d31c0b4e89e3">IUPnPDevices</a>
 

 

