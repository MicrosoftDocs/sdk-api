---
UID: NF:wsddisco.IWSDiscoveryProviderNotify.SearchComplete
title: IWSDiscoveryProviderNotify::SearchComplete (wsddisco.h)
description: Called to indicate a user initiated search has successfully completed and no more matches for the search will be accepted.
old-location: ncd\iwsdiscoveryprovidernotify_searchcomplete.htm
tech.root: WsdApi
ms.assetid: a125a7b3-6887-42e2-b421-d0e27973d8ee
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProviderNotify interface,SearchComplete method, IWSDiscoveryProviderNotify.SearchComplete, IWSDiscoveryProviderNotify::SearchComplete, SearchComplete, SearchComplete method, SearchComplete method,IWSDiscoveryProviderNotify interface, ncd.iwsdiscoveryprovidernotify_searchcomplete, wsddisco/IWSDiscoveryProviderNotify::SearchComplete
f1_keywords:
- wsddisco/IWSDiscoveryProviderNotify.SearchComplete
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryProviderNotify::SearchComplete


## -description


Called to indicate a user initiated search has successfully completed and no more matches for the search will be accepted.


## -parameters




### -param pszTag [in, optional]

Search tag passed to the <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> search method.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



If no responses are received for a given search, then <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchfailed">IWSDiscoveryProviderNotify::SearchFailed</a> will be called to indicate this.


The interval between initiating the search with <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype">SearchByType</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid">SearchById</a> and receiving a <b>SearchComplete</b> notification is a maximum of 10 seconds, based on MATCH_TIMEOUT from <a href="Http://go.microsoft.com/fwlink/p/?linkid=84393">WS-Discovery</a> and amended by the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84394">DPWS Appendix I</a>. The interval between initiating the search with <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress">SearchByAddress</a> and receiving a <b>SearchComplete</b> notification is a maximum of 150 seconds.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovidernotify">IWSDiscoveryProviderNotify</a>
 

 

