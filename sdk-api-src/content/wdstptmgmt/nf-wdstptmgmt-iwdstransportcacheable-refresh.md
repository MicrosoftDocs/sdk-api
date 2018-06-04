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

# IWdsTransportCacheable::Refresh


## -description


Refreshes the object data members by rereading their values from the underlying data store. This is allowed only if the object's <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">IWdsTransportCacheable::Dirty</a> property has been set.


## -parameters






## -remarks



When called on an object whose <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">Dirty</a> property has been set, this method fails in order to avoid inadvertently losing changes made to the object. If the caller wants to ignore current changes and reread the stored data, the caller should call the <a href="https://msdn.microsoft.com/5c8495b9-6c76-4bb0-8237-5f9008cefc91">IWdsTransportCacheable::Discard</a> method instead.




## -see-also




<a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a>
 

 

