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

# IWdsTransportCacheable::Discard


## -description


Discards all changes made to the object data members by clearing the <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">IWdsTransportCacheable::Dirty</a> property and then calling the object's <a href="https://msdn.microsoft.com/2fd838b5-5623-4133-9ad8-ec051b2b698d">IWdsTransportCacheable::Refresh</a> method to reread the current object data. 


## -parameters






## -remarks



This method can be called on any object. 

Unlike <a href="https://msdn.microsoft.com/2fd838b5-5623-4133-9ad8-ec051b2b698d">Refresh</a>, which always refreshes object data (as long as the object's <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">Dirty</a> property has been set), this method checks first that the object's <b>Dirty</b> property has been set. If it has, the method resets the <b>Dirty</b> property and then rereads the current values of all data members. If <b>Dirty</b> has not been set, this method takes no action and returns immediately.





## -see-also




<a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a>
 

 

