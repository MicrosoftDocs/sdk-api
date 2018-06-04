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

# IWdsTransportManager::GetWdsTransportServer


## -description


Creates an object of the <a href="https://msdn.microsoft.com/0129658d-8725-4020-ae9c-9d0a44075561">IWdsTransportServer</a> interface that can be used to manage a WDS transport server. The method confirms that the system can reach a WDS transport server with the specified name.


## -parameters




### -param bszServerName [in]

The name of the WDS transport server to be represented by this object. This can be a NetBIOS name or a fully qualified DNS name. If the value is an empty string, the object represents the local computer.


### -param ppWdsTransportServer [out]

A pointer to the object of the  <a href="https://msdn.microsoft.com/0129658d-8725-4020-ae9c-9d0a44075561">IWdsTransportServer</a> interface. 


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/23f36ec7-5f6f-486c-bb09-e2f5b6f57efa">IWdsTransportManager</a>



<a href="https://msdn.microsoft.com/0129658d-8725-4020-ae9c-9d0a44075561">IWdsTransportServer</a>
 

 

