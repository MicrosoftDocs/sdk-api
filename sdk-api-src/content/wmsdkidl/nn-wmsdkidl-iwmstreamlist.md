---
UID: NN:wmsdkidl.IWMStreamList
title: IWMStreamList
author: windows-sdk-content
description: The IWMStreamList interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams.
old-location: wmformat\iwmstreamlist.htm
tech.root: wmformat
ms.assetid: 076bb0bf-3cf8-48b4-bfca-abbd9c1bf211
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMStreamList, IWMStreamList interface [windows Media Format], IWMStreamList interface [windows Media Format],described, IWMStreamListInterface, wmformat.iwmstreamlist, wmsdkidl/IWMStreamList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStreamList interface


## -description



The <b>IWMStreamList</b> interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams. The <a href="https://msdn.microsoft.com/en-us/library/Dd757238(v=VS.85).aspx">IWMMutualExclusion</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd743298(v=VS.85).aspx">IWMBandwidthSharing</a> interfaces each inherit from <b>IWMStreamList</b>. These are the only uses of this interface in the SDK. You never need to deal with interface pointers for <b>IWMStreamList</b> directly.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMStreamList</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798570(v=VS.85).aspx">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798571(v=VS.85).aspx">GetStreams</a>
</td>
<td align="left" width="63%">
Retrieves an array of stream numbers that make up the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798572(v=VS.85).aspx">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the list.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/dd1f7865-e409-4bf9-9fa0-769a29eaed60">Mutual Exclusion Object</a>
 

 

