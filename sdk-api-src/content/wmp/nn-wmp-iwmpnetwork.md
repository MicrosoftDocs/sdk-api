---
UID: NN:wmp.IWMPNetwork
title: IWMPNetwork (wmp.h)
author: windows-sdk-content
description: The IWMPNetwork interface provides methods relating to the network connection used by Windows Media Player.
old-location: wmp\iwmpnetwork.htm
tech.root: WMP
ms.assetid: 074a4bc2-3d9f-4007-b6c8-91ea92a87b67
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], IWMPNetwork interface [Windows Media Player],described, IWMPNetworkInterface, wmp.iwmpnetwork, wmp/IWMPNetwork
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPNetwork interface


## -description



The <b>IWMPNetwork</b> interface provides methods relating to the network connection used by Windows Media Player.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPNetwork</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPNetwork</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563468(v=VS.85).aspx">get_bandWidth</a>
</td>
<td align="left" width="63%">
Retrieves the current bandwidth of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563469(v=VS.85).aspx">get_bitRate</a>
</td>
<td align="left" width="63%">
Retrieves the current bit rate being received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563470(v=VS.85).aspx">get_bufferingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times buffering occurred during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563471(v=VS.85).aspx">get_bufferingProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of buffering completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563472(v=VS.85).aspx">get_bufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of buffering time in milliseconds before playback begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563473(v=VS.85).aspx">get_downloadProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of downloading completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563474(v=VS.85).aspx">get_encodedFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the video frame rate specified by the content author.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563475(v=VS.85).aspx">get_frameRate</a>
</td>
<td align="left" width="63%">
Retrieves the current video frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563476(v=VS.85).aspx">get_framesSkipped</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames skipped during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563477(v=VS.85).aspx">get_lostPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of packets lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563478(v=VS.85).aspx">get_maxBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the maximum allowed bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563479(v=VS.85).aspx">get_maxBitRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum possible video bit rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563480(v=VS.85).aspx">get_receivedPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of packets received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563481(v=VS.85).aspx">get_receptionQuality</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of packets received in the last 30 seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563482(v=VS.85).aspx">get_recoveredPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of recovered packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563483(v=VS.85).aspx">get_sourceProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the source protocol used to receive the data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563462(v=VS.85).aspx">getProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the proxy server should be bypassed if the origin server is on a local network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563464(v=VS.85).aspx">getProxyExceptionList</a>
</td>
<td align="left" width="63%">
Retrieves the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563465(v=VS.85).aspx">getProxyName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a proxy server to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563466(v=VS.85).aspx">getProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the proxy port to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563467(v=VS.85).aspx">getProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the proxy settings for a given protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563484(v=VS.85).aspx">put_bufferingTime</a>
</td>
<td align="left" width="63%">
Specifies the amount of buffering time in milliseconds before playback begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563485(v=VS.85).aspx">put_maxBandwidth</a>
</td>
<td align="left" width="63%">
Specifies the maximum allowed bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563486(v=VS.85).aspx">setProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Specifies whether the proxy server is bypassed if the origin server is on a local network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563487(v=VS.85).aspx">setProxyExceptionList</a>
</td>
<td align="left" width="63%">
Specifies the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563488(v=VS.85).aspx">setProxyName</a>
</td>
<td align="left" width="63%">
Specifies the name of a proxy server to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563489(v=VS.85).aspx">setProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the proxy port to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563491(v=VS.85).aspx">setProxySettings</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563232(v=VS.85).aspx">get_network</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

