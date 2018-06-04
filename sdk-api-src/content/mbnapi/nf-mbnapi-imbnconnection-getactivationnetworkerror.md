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

# IMbnConnection::GetActivationNetworkError


## -description


Gets the network error returned in a Packet Data Protocol (PDP) context activation failure.


## -parameters




### -param networkError [out, retval]

The error code returned by the network from the last connection context activation operation.  The value is meaningful only if the method returns <b>S_OK</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For GSM devices these error codes are defined in 3GPP specification 24.008 as cause codes. For CDMA devices, device and network specific error codes are used.

The error codes are cleared when the context activation operation completes successfully. When there is no network error or the error is not known, then the value is set to 0.

Whenever there is a change in the network error value, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/5392e5b7-eac7-40f1-b5cd-adde5a6ff1b8">OnConnectStateChange</a> member of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>.





## -see-also




<a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a>
 

 

