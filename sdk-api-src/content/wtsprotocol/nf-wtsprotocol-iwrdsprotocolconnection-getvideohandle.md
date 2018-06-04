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

# IWRdsProtocolConnection::GetVideoHandle


## -description


Obtains the handle of the video device for the protocol.


## -parameters




### -param pVideoHandle [out]

A pointer to a handle that receives the handle of the video device.

If the protocol object is using the <a href="https://msdn.microsoft.com/ff8d2dd0-adbb-40de-a074-3228d803f4c8">IWRdsRemoteFXGraphicsConnection</a>  interface, this method should set the contents of <i>pVideoHandle</i> to <b>NULL</b> and return <b>E_NOTIMPL</b>.

If the protocol is not using the <a href="https://msdn.microsoft.com/ff8d2dd0-adbb-40de-a074-3228d803f4c8">IWRdsRemoteFXGraphicsConnection</a> interface, this method should return a handle to the video miniport driver for the remote session associated with the protocol.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

