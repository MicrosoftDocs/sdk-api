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

# IWdsTransportSession::RetrieveClients


## -description


Retrieves a collection of WDS clients joined to the transport session.


## -parameters




### -param ppWdsTransportClients [out]

A collection of objects of the <a href="https://msdn.microsoft.com/39534411-3d69-408d-b495-10851fe40bdf">IWdsTransportClient</a> interface joined to the transport session.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/39534411-3d69-408d-b495-10851fe40bdf">IWdsTransportClient</a>



<a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a>



<a href="https://msdn.microsoft.com/acf417ea-2396-4178-84e5-6d6b495476f8">IWdsTransportSession</a>
 

 

