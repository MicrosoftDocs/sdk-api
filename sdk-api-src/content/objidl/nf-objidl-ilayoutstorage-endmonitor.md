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

# ILayoutStorage::EndMonitor


## -description



			
			The <b>EndMonitor</b> method ends monitoring of a compound file. Must be preceded by a call to 
<a href="https://msdn.microsoft.com/16371d6c-adb9-43c2-80a4-377e94854bbb">ILayoutStorage::BeginMonitor</a>.


## -parameters






## -returns




						This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as all return values for <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.




## -remarks



A call to 
<b>EndMonitor</b> is generally followed by a call to 
<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ILayoutStorage::RelayoutDocfile</a>, which uses the access pattern detected by the monitoring to restructure the compound file.




## -see-also




<a href="https://msdn.microsoft.com/16371d6c-adb9-43c2-80a4-377e94854bbb">ILayoutStorage::BeginMonitor</a>



<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ILayoutStorage::ReLayoutDocfile</a>
 

 

