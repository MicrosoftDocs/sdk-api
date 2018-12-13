---
UID: NN:wmsdkidl.IWMReaderNetworkConfig2
title: IWMReaderNetworkConfig2
author: windows-sdk-content
description: The IWMReaderNetworkConfig2 interface provides advanced networking functionality.An IWMReaderNetworkConfig2 interface exists for every reader object.
old-location: wmformat\iwmreadernetworkconfig2.htm
tech.root: wmformat
ms.assetid: a0480243-53e0-4da5-a119-291b19f46951
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderNetworkConfig2, IWMReaderNetworkConfig2 interface [windows Media Format], IWMReaderNetworkConfig2 interface [windows Media Format],described, IWMReaderNetworkConfig2Interface, wmformat.iwmreadernetworkconfig2, wmsdkidl/IWMReaderNetworkConfig2
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
 - IWMReaderNetworkConfig2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig2 interface


## -description



The <b>IWMReaderNetworkConfig2</b> interface provides advanced networking functionality.

An <b>IWMReaderNetworkConfig2</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderNetworkConfig2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig</a>. <b>IWMReaderNetworkConfig2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743506(v=VS.85).aspx">GetAcceleratedStreamingDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of accelerated streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743507(v=VS.85).aspx">GetAutoReconnectLimit</a>
</td>
<td align="left" width="63%">
Retrieves the number of allowable automatic reconnections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743508(v=VS.85).aspx">GetEnableContentCaching</a>
</td>
<td align="left" width="63%">
Queries whether content caching is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743509(v=VS.85).aspx">GetEnableFastCache</a>
</td>
<td align="left" width="63%">
Queries whether Fast Cache streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743510(v=VS.85).aspx">GetEnableResends</a>
</td>
<td align="left" width="63%">
Queries whether resending is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743511(v=VS.85).aspx">GetEnableThinning</a>
</td>
<td align="left" width="63%">
Queries whether thinning is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743512(v=VS.85).aspx">GetMaxNetPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size of packets being delivered over a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743513(v=VS.85).aspx">SetAcceleratedStreamingDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of accelerated streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743514(v=VS.85).aspx">SetAutoReconnectLimit</a>
</td>
<td align="left" width="63%">
Sets the automatic reconnection limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743515(v=VS.85).aspx">SetEnableContentCaching</a>
</td>
<td align="left" width="63%">
Enables or disables content caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743516(v=VS.85).aspx">SetEnableFastCache</a>
</td>
<td align="left" width="63%">
Enables or disables Fast Cache streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743517(v=VS.85).aspx">SetEnableResends</a>
</td>
<td align="left" width="63%">
Enables or disables resending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743518(v=VS.85).aspx">SetEnableThinning</a>
</td>
<td align="left" width="63%">
Enables or disables thinning.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

