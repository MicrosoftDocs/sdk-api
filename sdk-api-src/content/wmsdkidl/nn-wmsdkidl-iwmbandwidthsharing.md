---
UID: NN:wmsdkidl.IWMBandwidthSharing
title: IWMBandwidthSharing (wmsdkidl.h)
author: windows-sdk-content
description: The IWMBandwidthSharing interface contains methods to manage the properties of combined streams.The list of streams that share bandwidth is stored in the bandwidth sharing object.
old-location: wmformat\iwmbandwidthsharing.htm
tech.root: wmformat
ms.assetid: fd0e48bb-2e5e-4158-9ff1-5b603f219689
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMBandwidthSharing, IWMBandwidthSharing interface [windows Media Format], IWMBandwidthSharing interface [windows Media Format],described, IWMBandwidthSharingInterface, wmformat.iwmbandwidthsharing, wmsdkidl/IWMBandwidthSharing
ms.topic: interface
f1_keywords: ["wmsdkidl/IWMBandwidthSharing"]
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
 - IWMBandwidthSharing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMBandwidthSharing interface


## -description



The <b>IWMBandwidthSharing</b> interface contains methods to manage the properties of combined streams.

The list of streams that share bandwidth is stored in the bandwidth sharing object. The streams can be manipulated using the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a> interface. <b>IWMBandwidthSharing</b> inherits from <b>IWMStreamList</b>, so the stream list manipulation methods are always exposed through this interface.

The information in a bandwidth sharing object is purely informational. Nothing in the SDK seeks to enforce or check the accuracy of the bandwidth specified. You might want to use bandwidth sharing so that a reading application can make adjustments based on the information contained in the bandwidth sharing object.

An <b>IWMBandwidthSharing</b> interface is exposed for each bandwidth sharing object upon creation. Bandwidth sharing objects are created using the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing">IWMProfile3::CreateNewBandwidthSharing</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMBandwidthSharing</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>. <b>IWMBandwidthSharing</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMBandwidthSharing</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-getbandwidth">GetBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth and maximum buffer size of the streams in the bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of sharing (exclusive or partial) for the bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-setbandwidth">SetBandwidth</a>
</td>
<td align="left" width="63%">
Sets the bandwidth and maximum buffer size for streams in the bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype">SetType</a>
</td>
<td align="left" width="63%">
Sets the type of sharing (exclusive or partial) for the bandwidth sharing object.

</td>
</tr>
</table> 

The following interface can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>
</td>
<td>IID_IWMStreamList</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/using-bandwidth-sharing">Using Bandwidth Sharing</a>
 

 

