---
UID: NN:wsddisco.IWSDiscoveryProviderNotify
title: IWSDiscoveryProviderNotify (wsddisco.h)
author: windows-sdk-content
description: Is implemented by the client program to receive callback notifications from IWSDiscoveryProvider.
old-location: ncd\iwsdiscoveryprovidernotify.htm
tech.root: WsdApi
ms.assetid: e186f721-14d9-4d9b-942a-1c05ada2bee6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProviderNotify, IWSDiscoveryProviderNotify interface, IWSDiscoveryProviderNotify interface,described, ncd.iwsdiscoveryprovidernotify, wsddisco/IWSDiscoveryProviderNotify
ms.topic: interface
f1_keywords: 
 - "wsddisco/IWSDiscoveryProviderNotify"
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
 - IWSDiscoveryProviderNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryProviderNotify interface


## -description


Is implemented by the client program to receive callback notifications from <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryProviderNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveryProviderNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDiscoveryProviderNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-add">Add</a>
</td>
<td align="left" width="63%">
Called to provide information on either a newly announced discovery host (from a Hello message), or a match to a user initiated query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-remove">Remove</a>
</td>
<td align="left" width="63%">
Called to provide information on a recently departed discovery host (from a Bye message).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchcomplete">SearchComplete</a>
</td>
<td align="left" width="63%">
Called to indicate a user initiated search has successfully completed and no more matches for the search will be accepted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-searchfailed">SearchFailed</a>
</td>
<td align="left" width="63%">
Called to indicate a user initiated search has failed.

</td>
</tr>
</table> 

