---
UID: NF:wsddisco.IWSDiscoveryProvider.SearchByType
title: IWSDiscoveryProvider::SearchByType (wsddisco.h)
description: Initializes a search for WS-Discovery hosts by device type.
helpviewer_keywords: ["IWSDiscoveryProvider interface","SearchByType method","IWSDiscoveryProvider.SearchByType","IWSDiscoveryProvider::SearchByType","SearchByType","SearchByType method","SearchByType method","IWSDiscoveryProvider interface","ncd.iwsdiscoveryprovider_searchbytype_method","wsddisco/IWSDiscoveryProvider::SearchByType"]
old-location: ncd\iwsdiscoveryprovider_searchbytype_method.htm
tech.root: ncd
ms.assetid: bb1f2822-4d5d-4156-99e3-5a4528474953
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProvider interface,SearchByType method, IWSDiscoveryProvider.SearchByType, IWSDiscoveryProvider::SearchByType, SearchByType, SearchByType method, SearchByType method,IWSDiscoveryProvider interface, ncd.iwsdiscoveryprovider_searchbytype_method, wsddisco/IWSDiscoveryProvider::SearchByType
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
 - IWSDiscoveryProvider::SearchByType
 - wsddisco/IWSDiscoveryProvider::SearchByType
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
 - IWSDiscoveryProvider.SearchByType
---

# IWSDiscoveryProvider::SearchByType


## -description

Initializes a search for <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery</a> hosts by device type.

## -parameters

### -param pTypesList [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that represents the list of discovery provider types to search for. May be <b>NULL</b>.

### -param pScopesList [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that represents the list of discovery provider scopes to search for. May be <b>NULL</b>.

### -param pszMatchBy [in, optional]

Matching rule used for scopes. May be <b>NULL</b>.

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
The length in characters of <i>pszMatchBy</i>  exceeds WSD_MAX_TEXT_LENGTH (8192) or the length in characters of  <i>pszTag</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

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

<b>SearchByType</b> initiates a WS-Discovery <a href="/windows/desktop/WsdApi/probe-message">Probe</a> in an attempt to locate discovery hosts matching the provided criteria. This method allows matching by types, scopes, some combination of the two, or matching all discovery capable devices (when no scopes or types are provided). 

<i>pszMatchBy</i> should be provided if and only if <i>pScopesList</i> is also provided. This call may result in one or more <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-add">Add</a> callbacks. If any <b>Add</b> callbacks are issued before the search completes, a <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchcomplete">SearchComplete</a> callback will be issued; otherwise, a <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchfailed">SearchFailed</a> callback will be issued.

<i>pszTag</i> is an optional user provided string which will be fed back in either callback, allowing the caller to associate the callback with the original query.

For information about troubleshooting applications calling this method, see <a href="/windows/desktop/WsdApi/troubleshooting-wsdapi-applications">Troubleshooting WSDAPI Applications</a>.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>