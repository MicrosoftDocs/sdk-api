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

# IEventClass interface


## -description


Associates a class of event objects with the event interface those objects implement.

<b>IEventClass</b> is the interface that is implemented by the CLSID_CEventClass objects, which are different than event class objects that are co-created by a publisher for the purpose of firing events.

An event object implements the <a href="https://msdn.microsoft.com/e603f68a-881c-468d-a3d3-738f43400e01">IMultiInterfaceEventControl</a> event interface. While this object can be used to configure event classes in the event store, the preferred method is to use the COM+ Administration interfaces. However, not all of the properties exposed by the <b>IEventClass</b> interface are available through the COM+ Administration interfaces.


## -see-also




<a href="https://msdn.microsoft.com/0e04cd6f-1f8b-4bdf-92b0-5baddeb361b5">COM+ Administration Interfaces</a>
 

 

