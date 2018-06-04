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

# IUPnPDeviceControl::GetServiceObject


## -description


The 
<b>GetServiceObject</b> method is used to obtain the <b>IDispatch</b> pointer to a specific service object. The device host invokes this method once per service, the first time it receives a request for a service.


## -parameters




### -param bstrUDN [in]

Specifies the UDN of the device.


### -param bstrServiceId [in]

Specifies the Service ID of the service for which to obtain the pointer.


### -param ppdispService






#### - pdispService [out]

Receives the <b>IDispatch</b> pointer to the service object.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -remarks



This method is invoked by the device host when a control request or event subscription is received for a particular service.

Embedded devices are differentiated by their UDNs.




## -see-also




<a href="https://msdn.microsoft.com/c5d68459-f4ba-4df1-a00c-be86e24ce29f">IUPnPDeviceControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
 

 

