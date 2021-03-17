---
UID: NF:wsddisco.IWSDiscoveryProvider.SearchById
title: IWSDiscoveryProvider::SearchById (wsddisco.h)
description: Initializes a search for WS-Discovery hosts by device identifier.
helpviewer_keywords: ["IWSDiscoveryProvider interface","SearchById method","IWSDiscoveryProvider.SearchById","IWSDiscoveryProvider::SearchById","SearchById","SearchById method","SearchById method","IWSDiscoveryProvider interface","ncd.iwsdiscoveryprovider_searchbyid","wsddisco/IWSDiscoveryProvider::SearchById"]
old-location: ncd\iwsdiscoveryprovider_searchbyid.htm
tech.root: ncd
ms.assetid: 78ae714a-1ee3-46eb-b3d6-ff46bf8974ab
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProvider interface,SearchById method, IWSDiscoveryProvider.SearchById, IWSDiscoveryProvider::SearchById, SearchById, SearchById method, SearchById method,IWSDiscoveryProvider interface, ncd.iwsdiscoveryprovider_searchbyid, wsddisco/IWSDiscoveryProvider::SearchById
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
 - IWSDiscoveryProvider::SearchById
 - wsddisco/IWSDiscoveryProvider::SearchById
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDiscoveryProvider.SearchById
---

# IWSDiscoveryProvider::SearchById


## -description

Initializes a search for <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery</a> hosts by device identifier.

## -parameters

### -param pszId [in]

Device identifier of the desired discovery provider.

### -param pszTag [in, optional]

Optional identifier tag for this search.  May be <b>NULL</b>.

## -returns

Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszId</i> is <b>NULL</b>, the length in characters of <i>pszId</i>  exceeds WSD_MAX_TEXT_LENGTH (8192), or the length in characters of  <i>pszTag</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has not been attached. You must call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-attach">Attach</a> before calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

<b>SearchById</b> initiates a WS-Discovery <a href="/windows/desktop/WsdApi/resolve-message">Resolve</a> in an attempt to locate a previously known specific device. <i>pszId</i> is used as the endpoint address in the Resolve. This call may result in one or more <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-add">Add</a> callbacks. If any <b>Add</b> callbacks are issued before the search completes, a <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchcomplete">SearchComplete</a> callback will be issued; otherwise, a <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchfailed">SearchFailed</a> callback will be issued.

<i>pszTag</i> is an optional user provided string which will be fed back in either callback, allowing the caller to associate the callback with the original query.

For information about troubleshooting applications calling this method, see <a href="/windows/desktop/WsdApi/troubleshooting-wsdapi-applications">Troubleshooting WSDAPI Applications</a>.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>