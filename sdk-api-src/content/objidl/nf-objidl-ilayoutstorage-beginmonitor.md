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

# ILayoutStorage::BeginMonitor


## -description



			The <b>BeginMonitor</b> method is used to begin monitoring when a loading operation is started. When the operation is complete, the application must call 
<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">ILayoutStorage::EndMonitor</a>.


## -parameters






## -returns




						This method supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:




## -remarks



Normally an application calls 
<b>BeginMonitor</b> before the actual loading begins. Once this method has been called, the compound file implementation regards any operation performed on the files storages and streams as part of the desired access pattern. The result is a layout script like that created explicitly by calling 
<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">ILayoutStorage::LayoutScript</a>.

Applications will usually use monitoring to obtain the access pattern of embedded objects. Monitoring also makes possible generic layout tools,  that launch existing applications and monitor their access patterns.

A call to 
<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">ILayoutStorage::EndMonitor</a> ends monitoring. Multiple calls to 
<b>BeginMonitor</b> and
<b>EndMonitor</b> are permitted. Monitoring can also be mixed with calls to 
<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">ILayoutStorage::LayoutScript</a>.




## -see-also




<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">ILayoutStorage::EndMonitor</a>



<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">ILayoutStorage::LayoutScript</a>
 

 

