---
UID: NN:wmp.IWMPNetwork
title: IWMPNetwork (wmp.h)
description: The IWMPNetwork interface provides methods relating to the network connection used by Windows Media Player.
helpviewer_keywords: ["IWMPNetwork","IWMPNetwork interface [Windows Media Player]","IWMPNetwork interface [Windows Media Player]","described","IWMPNetworkInterface","wmp.iwmpnetwork","wmp/IWMPNetwork"]
old-location: wmp\iwmpnetwork.htm
tech.root: WMP
ms.assetid: 074a4bc2-3d9f-4007-b6c8-91ea92a87b67
ms.date: 12/05/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], IWMPNetwork interface [Windows Media Player],described, IWMPNetworkInterface, wmp.iwmpnetwork, wmp/IWMPNetwork
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPNetwork
 - wmp/IWMPNetwork
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPNetwork
---

# IWMPNetwork interface


## -description

The <b>IWMPNetwork</b> interface provides methods relating to the network connection used by Windows Media Player.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPNetwork</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPNetwork</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bandwidth">get_bandWidth</a>
</td>
<td align="left" width="63%">
Retrieves the current bandwidth of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bitrate">get_bitRate</a>
</td>
<td align="left" width="63%">
Retrieves the current bit rate being received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bufferingcount">get_bufferingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times buffering occurred during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bufferingprogress">get_bufferingProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of buffering completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bufferingtime">get_bufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of buffering time in milliseconds before playback begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_downloadprogress">get_downloadProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of downloading completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_encodedframerate">get_encodedFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the video frame rate specified by the content author.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_framerate">get_frameRate</a>
</td>
<td align="left" width="63%">
Retrieves the current video frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_framesskipped">get_framesSkipped</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames skipped during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_lostpackets">get_lostPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of packets lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_maxbandwidth">get_maxBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the maximum allowed bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_maxbitrate">get_maxBitRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum possible video bit rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_receivedpackets">get_receivedPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of packets received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_receptionquality">get_receptionQuality</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of packets received in the last 30 seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_recoveredpackets">get_recoveredPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of recovered packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_sourceprotocol">get_sourceProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the source protocol used to receive the data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxybypassforlocal">getProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the proxy server should be bypassed if the origin server is on a local network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxyexceptionlist">getProxyExceptionList</a>
</td>
<td align="left" width="63%">
Retrieves the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxyname">getProxyName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a proxy server to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxyport">getProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the proxy port to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">getProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the proxy settings for a given protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-put_bufferingtime">put_bufferingTime</a>
</td>
<td align="left" width="63%">
Specifies the amount of buffering time in milliseconds before playback begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-put_maxbandwidth">put_maxBandwidth</a>
</td>
<td align="left" width="63%">
Specifies the maximum allowed bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxybypassforlocal">setProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Specifies whether the proxy server is bypassed if the origin server is on a local network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxyexceptionlist">setProxyExceptionList</a>
</td>
<td align="left" width="63%">
Specifies the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxyname">setProxyName</a>
</td>
<td align="left" width="63%">
Specifies the name of a proxy server to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxyport">setProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the proxy port to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxysettings">setProxySettings</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_network">get_network</a>
</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>

