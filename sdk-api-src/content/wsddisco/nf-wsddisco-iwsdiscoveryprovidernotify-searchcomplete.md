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

# IWSDiscoveryProviderNotify::SearchComplete


## -description


Called to indicate a user initiated search has successfully completed and no more matches for the search will be accepted.


## -parameters




### -param pszTag [in, optional]

Search tag passed to the <a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a> search method.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



If no responses are received for a given search, then <a href="https://msdn.microsoft.com/8f861c69-2967-4a8d-a64a-e2409d722984">IWSDiscoveryProviderNotify::SearchFailed</a> will be called to indicate this.


The interval between initiating the search with <a href="https://msdn.microsoft.com/bb1f2822-4d5d-4156-99e3-5a4528474953">SearchByType</a> or <a href="https://msdn.microsoft.com/78ae714a-1ee3-46eb-b3d6-ff46bf8974ab">SearchById</a> and receiving a <b>SearchComplete</b> notification is a maximum of 10 seconds, based on MATCH_TIMEOUT from <a href="Http://go.microsoft.com/fwlink/p/?linkid=84393">WS-Discovery</a> and amended by the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84394">DPWS Appendix I</a>. The interval between initiating the search with <a href="https://msdn.microsoft.com/64493841-0715-4bae-a416-aca9945b2420">SearchByAddress</a> and receiving a <b>SearchComplete</b> notification is a maximum of 150 seconds.




## -see-also




<a href="https://msdn.microsoft.com/e186f721-14d9-4d9b-942a-1c05ada2bee6">IWSDiscoveryProviderNotify</a>
 

 

