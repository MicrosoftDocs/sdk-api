---
UID: NN:wmp.IWMPNetwork
title: IWMPNetwork
author: windows-sdk-content
description: The IWMPNetwork interface provides methods relating to the network connection used by Windows Media Player.
old-location: wmp\iwmpnetwork.htm
old-project: WMP
ms.assetid: 074a4bc2-3d9f-4007-b6c8-91ea92a87b67
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], IWMPNetwork interface [Windows Media Player],described, IWMPNetworkInterface, wmp.iwmpnetwork, wmp/IWMPNetwork
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
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
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPNetwork
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork interface


## -description



The <b>IWMPNetwork</b> interface provides methods relating to the network connection used by Windows Media Player.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPNetwork</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPNetwork</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPNetwork</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/910356d8-3d43-4516-ad30-b0ed288e5098">get_bandWidth</a>
</td>
<td align="left" width="63%">
Retrieves the current bandwidth of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfac8b29-47d9-4cee-801b-f43fa2bba6ed">get_bitRate</a>
</td>
<td align="left" width="63%">
Retrieves the current bit rate being received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ba9be8d-9b2b-4620-8572-317555d51bdf">get_bufferingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times buffering occurred during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c8cc541-3fc2-49b8-8a1a-f4959989aafe">get_bufferingProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of buffering completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a42a7187-9bf2-4db5-8176-6912e18c4d50">get_bufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of buffering time in milliseconds before playback begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ed2027-cba4-4701-a416-a2190b51570c">get_downloadProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of downloading completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d42133cf-3b81-4d22-b83d-d8a5756d9d9c">get_encodedFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the video frame rate specified by the content author.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1521c462-b054-46d6-8646-4d20a836eadc">get_frameRate</a>
</td>
<td align="left" width="63%">
Retrieves the current video frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ca3e280-4f3e-4460-884d-186199e3edd6">get_framesSkipped</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames skipped during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/821b9bfc-931c-4e83-a899-4755bad3e7ae">get_lostPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of packets lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b1b845-7aa5-49d7-a9da-52dea06e51c4">get_maxBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the maximum allowed bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42917ca3-07d3-4d32-a2f3-5f0ef9d387d7">get_maxBitRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum possible video bit rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a896a67-ef0c-4fd7-b352-3c091bea1ad8">get_receivedPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of packets received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/835f56a4-26d3-480c-bf3e-49c269e9cc5a">get_receptionQuality</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of packets received in the last 30 seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c1b41c3-286c-4d1f-ab2f-ce088289eaae">get_recoveredPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of recovered packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6703ce88-9ca8-4401-b297-f765c4b15b84">get_sourceProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the source protocol used to receive the data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33cc24ab-9eb4-48ef-9483-058a3af04983">getProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the proxy server should be bypassed if the origin server is on a local network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddd3a6b2-3637-4da1-b3ce-f01364e8b818">getProxyExceptionList</a>
</td>
<td align="left" width="63%">
Retrieves the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bf3adaa-a89d-4ffe-8233-a9c606b39350">getProxyName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a proxy server to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d636e61-a5c1-495a-8d1d-ce2937dd3f18">getProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the proxy port to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/103e0d53-943d-4aba-9db1-20cdc1d75d52">getProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the proxy settings for a given protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f25992f-e3a0-477b-b445-1f3fb7d9eae1">put_bufferingTime</a>
</td>
<td align="left" width="63%">
Specifies the amount of buffering time in milliseconds before playback begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7259a5e2-dbc6-4ac0-946e-e79d542edb06">put_maxBandwidth</a>
</td>
<td align="left" width="63%">
Specifies the maximum allowed bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4477bc81-e52b-4924-a31b-6f005a5bd158">setProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Specifies whether the proxy server is bypassed if the origin server is on a local network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af9202aa-fa4e-4726-908f-3fc5370e06df">setProxyExceptionList</a>
</td>
<td align="left" width="63%">
Specifies the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f484f5b-195c-496d-932e-3e1fdbf873d8">setProxyName</a>
</td>
<td align="left" width="63%">
Specifies the name of a proxy server to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36b7290d-c359-45bb-b77b-46b696e9edcf">setProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the proxy port to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ce07bf8-8521-4240-9859-3bf790ccbf48">setProxySettings</a>
</td>
<td align="left" width="63%">
Specifies the proxy settings for a given protocol.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPNetwork</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/8100008a-50da-4496-9d5a-77bcca94e903">get_network</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

