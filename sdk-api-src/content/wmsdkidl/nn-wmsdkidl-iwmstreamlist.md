---
UID: NN:wmsdkidl.IWMStreamList
title: IWMStreamList (wmsdkidl.h)
description: The IWMStreamList interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams.
old-location: wmformat\iwmstreamlist.htm
tech.root: wmformat
ms.assetid: 076bb0bf-3cf8-48b4-bfca-abbd9c1bf211
ms.date: 12/05/2018
ms.keywords: IWMStreamList, IWMStreamList interface [windows Media Format], IWMStreamList interface [windows Media Format],described, IWMStreamListInterface, wmformat.iwmstreamlist, wmsdkidl/IWMStreamList
f1_keywords:
- wmsdkidl/IWMStreamList
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMStreamList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamList interface


## -description



The <b>IWMStreamList</b> interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams. The <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interfaces each inherit from <b>IWMStreamList</b>. These are the only uses of this interface in the SDK. You never need to deal with interface pointers for <b>IWMStreamList</b> directly.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStreamList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStreamList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamlist-getstreams">GetStreams</a>
</td>
<td align="left" width="63%">
Retrieves an array of stream numbers that make up the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamlist-removestream">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the list.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/mutual-exclusion-object">Mutual Exclusion Object</a>
 

 

