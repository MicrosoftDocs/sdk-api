---
UID: NN:wmsdkidl.IWMStreamList
title: IWMStreamList
author: windows-sdk-content
description: The IWMStreamList interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams.
old-location: wmformat\iwmstreamlist.htm
old-project: wmformat
ms.assetid: 076bb0bf-3cf8-48b4-bfca-abbd9c1bf211
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMStreamList, IWMStreamList interface [windows Media Format], IWMStreamList interface [windows Media Format],described, IWMStreamListInterface, wmformat.iwmstreamlist, wmsdkidl/IWMStreamList
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamList interface


## -description



The <b>IWMStreamList</b> interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams. The <a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion</a> and <a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing</a> interfaces each inherit from <b>IWMStreamList</b>. These are the only uses of this interface in the SDK. You never need to deal with interface pointers for <b>IWMStreamList</b> directly.




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
<a href="https://msdn.microsoft.com/20aeed9d-029b-4b60-9ff3-14555bd53eb9">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef7e1141-284f-4570-8891-9f53b2da7229">GetStreams</a>
</td>
<td align="left" width="63%">
Retrieves an array of stream numbers that make up the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b69f516-a321-49f1-a299-666143eaf8a5">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the list.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/dd1f7865-e409-4bf9-9fa0-769a29eaed60">Mutual Exclusion Object</a>
 

 

