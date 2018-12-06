---
UID: NF:wsddisco.IWSDiscoveryProviderNotify.SearchComplete
title: IWSDiscoveryProviderNotify::SearchComplete
author: windows-sdk-content
description: Called to indicate a user initiated search has successfully completed and no more matches for the search will be accepted.
old-location: ncd\iwsdiscoveryprovidernotify_searchcomplete.htm
tech.root: wsdapi
ms.assetid: a125a7b3-6887-42e2-b421-d0e27973d8ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDiscoveryProviderNotify interface,SearchComplete method, IWSDiscoveryProviderNotify.SearchComplete, IWSDiscoveryProviderNotify::SearchComplete, SearchComplete, SearchComplete method, SearchComplete method,IWSDiscoveryProviderNotify interface, ncd.iwsdiscoveryprovidernotify_searchcomplete, wsddisco/IWSDiscoveryProviderNotify::SearchComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProviderNotify.SearchComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

