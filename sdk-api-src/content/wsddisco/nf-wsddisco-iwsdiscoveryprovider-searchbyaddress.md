---
UID: NF:wsddisco.IWSDiscoveryProvider.SearchByAddress
title: IWSDiscoveryProvider::SearchByAddress (wsddisco.h)
description: Initializes a search for WS-Discovery hosts by device address.
helpviewer_keywords: ["IWSDiscoveryProvider interface","SearchByAddress method","IWSDiscoveryProvider.SearchByAddress","IWSDiscoveryProvider::SearchByAddress","SearchByAddress","SearchByAddress method","SearchByAddress method","IWSDiscoveryProvider interface","ncd.iwsdiscoveryprovider_searchbyaddress","wsddisco/IWSDiscoveryProvider::SearchByAddress"]
old-location: ncd\iwsdiscoveryprovider_searchbyaddress.htm
tech.root: ncd
ms.assetid: 64493841-0715-4bae-a416-aca9945b2420
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProvider interface,SearchByAddress method, IWSDiscoveryProvider.SearchByAddress, IWSDiscoveryProvider::SearchByAddress, SearchByAddress, SearchByAddress method, SearchByAddress method,IWSDiscoveryProvider interface, ncd.iwsdiscoveryprovider_searchbyaddress, wsddisco/IWSDiscoveryProvider::SearchByAddress
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
 - IWSDiscoveryProvider::SearchByAddress
 - wsddisco/IWSDiscoveryProvider::SearchByAddress
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
 - IWSDiscoveryProvider.SearchByAddress
---

# IWSDiscoveryProvider::SearchByAddress


## -description

Initializes a search for <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery</a> hosts by device address.

## -parameters

### -param pszAddress [in]

The HTTP transport address of the device.

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
<i>pszAddress</i> is <b>NULL</b>, the length in characters of <i>pszAddress</i>  exceeds WSD_MAX_TEXT_LENGTH (8192), or the length in characters of  <i>pszTag</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

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

<b>SearchByAddress</b> initiates a WS-Discovery <a href="/windows/desktop/WsdApi/probe-message">Probe</a> over HTTP in an attempt to identify a device at a known URL. The Probe is sent to the address specified by <i>pszAddress</i>. This call may result in one or more <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-add">Add</a> callbacks. If any <b>Add</b> callbacks are issued before the search completes, a <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchcomplete">SearchComplete</a> callback will be issued; otherwise, a <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchfailed">SearchFailed</a> callback will be issued.  The interval between initiating the search and receiving either of these notifications can be up to 30 seconds.

<i>pszTag</i> is an optional user provided string which will be fed back in either callback, allowing the caller to associate the callback with the original query.

For information about troubleshooting applications calling this method, see <a href="/windows/desktop/WsdApi/troubleshooting-wsdapi-applications">Troubleshooting WSDAPI Applications</a>.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>