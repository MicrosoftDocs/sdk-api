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

# IWRdsProtocolConnection::CreateVirtualChannel


## -description


Requests that the protocol create a virtual channel.


## -parameters




### -param szEndpointName [in]

A null-terminated string that contains the endpoint data that uniquely identifies the connection.


### -param bStatic [in]

Specifies whether the virtual channel is static or dynamic.



#### TRUE

The channel is static.



#### FALSE

The channel is dynamic.


### -param RequestedPriority [in]

Specifies the requested priority for the channel.


### -param phChannel [out]

A pointer to a <b>ULONG</b> value that receives the handle for the channel created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Virtual channels are software extensions that can be created to enhance a Remote Desktop Services application. Examples include support for additional hardware or additions to the functionality provided by a given protocol. For more information, see <a href="https://msdn.microsoft.com/f7bdebec-ecc3-4f28-9327-f0d2f169c142">Remote Desktop Services Virtual 
      Channels</a>.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

