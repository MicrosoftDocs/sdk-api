---
UID: NN:wmsdkidl.IWMReaderNetworkConfig2
title: IWMReaderNetworkConfig2 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderNetworkConfig2 interface provides advanced networking functionality.An IWMReaderNetworkConfig2 interface exists for every reader object.
old-location: wmformat\iwmreadernetworkconfig2.htm
tech.root: wmformat
ms.assetid: a0480243-53e0-4da5-a119-291b19f46951
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig2, IWMReaderNetworkConfig2 interface [windows Media Format], IWMReaderNetworkConfig2 interface [windows Media Format],described, IWMReaderNetworkConfig2Interface, wmformat.iwmreadernetworkconfig2, wmsdkidl/IWMReaderNetworkConfig2
ms.topic: interface
f1_keywords: ["wmsdkidl/IWMReaderNetworkConfig2"]
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
 - IWMReaderNetworkConfig2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig2 interface


## -description



The <b>IWMReaderNetworkConfig2</b> interface provides advanced networking functionality.

An <b>IWMReaderNetworkConfig2</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderNetworkConfig2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig</a>. <b>IWMReaderNetworkConfig2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderNetworkConfig2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getacceleratedstreamingduration">GetAcceleratedStreamingDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of accelerated streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getautoreconnectlimit">GetAutoReconnectLimit</a>
</td>
<td align="left" width="63%">
Retrieves the number of allowable automatic reconnections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getenablecontentcaching">GetEnableContentCaching</a>
</td>
<td align="left" width="63%">
Queries whether content caching is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getenablefastcache">GetEnableFastCache</a>
</td>
<td align="left" width="63%">
Queries whether Fast Cache streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getenableresends">GetEnableResends</a>
</td>
<td align="left" width="63%">
Queries whether resending is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getenablethinning">GetEnableThinning</a>
</td>
<td align="left" width="63%">
Queries whether thinning is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getmaxnetpacketsize">GetMaxNetPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size of packets being delivered over a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setacceleratedstreamingduration">SetAcceleratedStreamingDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of accelerated streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setautoreconnectlimit">SetAutoReconnectLimit</a>
</td>
<td align="left" width="63%">
Sets the automatic reconnection limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching">SetEnableContentCaching</a>
</td>
<td align="left" width="63%">
Enables or disables content caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache">SetEnableFastCache</a>
</td>
<td align="left" width="63%">
Enables or disables Fast Cache streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenableresends">SetEnableResends</a>
</td>
<td align="left" width="63%">
Enables or disables resending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablethinning">SetEnableThinning</a>
</td>
<td align="left" width="63%">
Enables or disables thinning.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

