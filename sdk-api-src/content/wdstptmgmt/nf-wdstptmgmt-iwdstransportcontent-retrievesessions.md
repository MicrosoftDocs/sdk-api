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

# IWdsTransportContent::RetrieveSessions


## -description


Retrieves a collection of active transport sessions associated with this content.


## -parameters




### -param ppWdsTransportSessions [out]

A pointer to a collection of objects of the <a href="https://msdn.microsoft.com/acf417ea-2396-4178-84e5-6d6b495476f8">IWdsTransportSession</a> interface that represent active sessions under this content.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/d7ed1f64-578f-4b3a-b9af-9a48800b9ca4">IWdsTransportContent</a>
 

 

