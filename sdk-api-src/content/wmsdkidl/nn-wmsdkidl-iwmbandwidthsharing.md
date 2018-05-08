---
UID: NN:wmsdkidl.IWMBandwidthSharing
title: IWMBandwidthSharing
author: windows-driver-content
description: The IWMBandwidthSharing interface contains methods to manage the properties of combined streams.The list of streams that share bandwidth is stored in the bandwidth sharing object.
old-location: wmformat\iwmbandwidthsharing.htm
old-project: wmformat
ms.assetid: fd0e48bb-2e5e-4158-9ff1-5b603f219689
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMBandwidthSharing, IWMBandwidthSharing interface [windows Media Format], IWMBandwidthSharing interface [windows Media Format],described, IWMBandwidthSharingInterface, wmformat.iwmbandwidthsharing, wmsdkidl/IWMBandwidthSharing
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMBandwidthSharing
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMBandwidthSharing interface


## -description



The <b>IWMBandwidthSharing</b> interface contains methods to manage the properties of combined streams.

The list of streams that share bandwidth is stored in the bandwidth sharing object. The streams can be manipulated using the methods of the <a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a> interface. <b>IWMBandwidthSharing</b> inherits from <b>IWMStreamList</b>, so the stream list manipulation methods are always exposed through this interface.

The information in a bandwidth sharing object is purely informational. Nothing in the SDK seeks to enforce or check the accuracy of the bandwidth specified. You might want to use bandwidth sharing so that a reading application can make adjustments based on the information contained in the bandwidth sharing object.

An <b>IWMBandwidthSharing</b> interface is exposed for each bandwidth sharing object upon creation. Bandwidth sharing objects are created using the <a href="https://msdn.microsoft.com/ab6c9903-95ea-499b-be75-ff57328336f0">IWMProfile3::CreateNewBandwidthSharing</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMBandwidthSharing</b> interface inherits from <a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>. <b>IWMBandwidthSharing</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2769328c-5c05-49fb-bfa6-729115dd417e">GetBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth and maximum buffer size of the streams in the bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of sharing (exclusive or partial) for the bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f2ac613-3674-46d9-ae7c-26389dbede02">SetBandwidth</a>
</td>
<td align="left" width="63%">
Sets the bandwidth and maximum buffer size for streams in the bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991816">SetType</a>
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
<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>
</td>
<td>IID_IWMStreamList</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>



<a href="https://msdn.microsoft.com/1df61a3a-d34a-447e-a7ee-d5d409e7c4fa">Using Bandwidth Sharing</a>
 

 

