---
UID: NN:wmsdkidl.IWMReaderNetworkConfig2
title: IWMReaderNetworkConfig2
author: windows-sdk-content
description: The IWMReaderNetworkConfig2 interface provides advanced networking functionality.An IWMReaderNetworkConfig2 interface exists for every reader object.
old-location: wmformat\iwmreadernetworkconfig2.htm
old-project: wmformat
ms.assetid: a0480243-53e0-4da5-a119-291b19f46951
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMReaderNetworkConfig2, IWMReaderNetworkConfig2 interface [windows Media Format], IWMReaderNetworkConfig2 interface [windows Media Format],described, IWMReaderNetworkConfig2Interface, wmformat.iwmreadernetworkconfig2, wmsdkidl/IWMReaderNetworkConfig2
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
 - IWMReaderNetworkConfig2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2 interface


## -description



The <b>IWMReaderNetworkConfig2</b> interface provides advanced networking functionality.

An <b>IWMReaderNetworkConfig2</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderNetworkConfig2</b> interface inherits from <a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig</a>. <b>IWMReaderNetworkConfig2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a8feda02-113a-4763-b695-c4cd48781ade">GetAcceleratedStreamingDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of accelerated streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d0b794c-b3bf-4ec5-ac68-9666e73f7a6e">GetAutoReconnectLimit</a>
</td>
<td align="left" width="63%">
Retrieves the number of allowable automatic reconnections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8fdbb18-ba50-47e7-b7c9-858e6c452071">GetEnableContentCaching</a>
</td>
<td align="left" width="63%">
Queries whether content caching is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50f904a3-5a2d-4c0f-92fe-76a1ff195c91">GetEnableFastCache</a>
</td>
<td align="left" width="63%">
Queries whether Fast Cache streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d39d42c3-7d00-4fb6-8979-2b65d00ac636">GetEnableResends</a>
</td>
<td align="left" width="63%">
Queries whether resending is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ad43406-56db-48db-96a7-419b6719dbd4">GetEnableThinning</a>
</td>
<td align="left" width="63%">
Queries whether thinning is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0249822c-4772-4317-aec2-e466fbd70bad">GetMaxNetPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size of packets being delivered over a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9ad5064-7742-4145-b560-f3e867da609a">SetAcceleratedStreamingDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of accelerated streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ef6bb5c-6369-4b80-a227-da790b1ab6da">SetAutoReconnectLimit</a>
</td>
<td align="left" width="63%">
Sets the automatic reconnection limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68dcb12e-e254-407e-864b-54d4e84b08ed">SetEnableContentCaching</a>
</td>
<td align="left" width="63%">
Enables or disables content caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28a01985-a133-4203-8385-d4497c29bf9c">SetEnableFastCache</a>
</td>
<td align="left" width="63%">
Enables or disables Fast Cache streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3bd0e03-eee1-4022-8540-1dcc927d6b5f">SetEnableResends</a>
</td>
<td align="left" width="63%">
Enables or disables resending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98d4eb7e-e712-4ca0-a532-1160254748b8">SetEnableThinning</a>
</td>
<td align="left" width="63%">
Enables or disables thinning.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

