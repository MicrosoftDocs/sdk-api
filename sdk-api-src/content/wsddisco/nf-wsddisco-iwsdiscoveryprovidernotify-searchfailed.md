---
UID: NF:wsddisco.IWSDiscoveryProviderNotify.SearchFailed
title: IWSDiscoveryProviderNotify::SearchFailed (wsddisco.h)
description: Is called to indicate a user initiated search has failed.
helpviewer_keywords: ["IWSDiscoveryProviderNotify interface","SearchFailed method","IWSDiscoveryProviderNotify.SearchFailed","IWSDiscoveryProviderNotify::SearchFailed","SearchFailed","SearchFailed method","SearchFailed method","IWSDiscoveryProviderNotify interface","ncd.iwsdiscoveryprovidernotify_searchfailed_method","wsddisco/IWSDiscoveryProviderNotify::SearchFailed"]
old-location: ncd\iwsdiscoveryprovidernotify_searchfailed_method.htm
tech.root: ncd
ms.assetid: 8f861c69-2967-4a8d-a64a-e2409d722984
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProviderNotify interface,SearchFailed method, IWSDiscoveryProviderNotify.SearchFailed, IWSDiscoveryProviderNotify::SearchFailed, SearchFailed, SearchFailed method, SearchFailed method,IWSDiscoveryProviderNotify interface, ncd.iwsdiscoveryprovidernotify_searchfailed_method, wsddisco/IWSDiscoveryProviderNotify::SearchFailed
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveryProviderNotify::SearchFailed
 - wsddisco/IWSDiscoveryProviderNotify::SearchFailed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProviderNotify.SearchFailed
---

# IWSDiscoveryProviderNotify::SearchFailed


## -description

Is called to indicate a user initiated search has failed.

## -parameters

### -param hr [in]

Cause of the search failure which initiated this callback.  A value of <b>S_FALSE</b> indicates the search completed without issuing any Add callbacks.

### -param pszTag [in, optional]

Optional identifier tag for this search.  May be <b>NULL</b>.

## -returns

The return value is not meaningful.  An implementer should return <b>S_OK</b>.

## -remarks

<a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchcomplete">SearchComplete</a> is called if any responses were successfully received.

<b>SearchFailed</b> is called if a user initiated query does not result in a response. In this case, the value of the <i>hr</i> parameter will be S_FALSE.  <b>SearchFailed</b> can optionally be called if errors occur in the attempted transmission of the query, since query transmission is not necessarily synchronous. <i>pszTag</i> will match the user supplied tag from the query, and should be used to identify which query failed. 

The interval between initiating the search with <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype">SearchByType</a> or <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid">SearchById</a>  and receiving a <b>SearchFailed</b> notification is a maximum of 10 seconds, based on MATCH_TIMEOUT from <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery</a> and amended by the <a href="https://specs.xmlsoap.org/ws/2005/05/devprof/devicesprofile.pdf">DPWS Appendix I</a>. The interval between initiating the search with <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress">SearchByAddress</a> and receipt of a <b>SearchFailed</b> notification is typically 21 seconds, but can be a maximum of 150 seconds.

<div class="alert"><b>Note</b>  Multiple simultaneous calls may be made to <b>SearchFailed</b> by the provider, so it is essential that shared data be synchronized in this callback.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovidernotify">IWSDiscoveryProviderNotify</a>