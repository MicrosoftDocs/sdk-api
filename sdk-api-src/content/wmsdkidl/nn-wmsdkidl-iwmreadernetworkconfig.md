---
UID: NN:wmsdkidl.IWMReaderNetworkConfig
title: IWMReaderNetworkConfig (wmsdkidl.h)
description: The IWMReaderNetworkConfig interface is used to set and test network configuration settings.
helpviewer_keywords: ["IWMReaderNetworkConfig","IWMReaderNetworkConfig interface [windows Media Format]","IWMReaderNetworkConfig interface [windows Media Format]","described","IWMReaderNetworkConfigInterface","wmformat.iwmreadernetworkconfig","wmsdkidl/IWMReaderNetworkConfig"]
old-location: wmformat\iwmreadernetworkconfig.htm
tech.root: wmformat
ms.assetid: 0957ece7-93fe-411b-b69e-fd03933b09d1
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], IWMReaderNetworkConfig interface [windows Media Format],described, IWMReaderNetworkConfigInterface, wmformat.iwmreadernetworkconfig, wmsdkidl/IWMReaderNetworkConfig
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig
dev_langs:
- c++
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
- IWMReaderNetworkConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig interface


## -description



The <b>IWMReaderNetworkConfig</b> interface is used to set and test network configuration settings. By using this interface, the application can configure which protocols must be used to receive the stream as well as other advanced network settings, such as proxy specification and buffering time.

An <b>IWMReaderNetworkConfig</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderNetworkConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderNetworkConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderNetworkConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl">AddLoggingUrl</a>
</td>
<td align="left" width="63%">
Adds the specified URL to the list of URLs to receive logging data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getbufferingtime">GetBufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of time required by the network source to buffer data before rendering it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getconnectionbandwidth">GetConnectionBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the connection bandwidth for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenablehttp">GetEnableHTTP</a>
</td>
<td align="left" width="63%">
Ascertains whether Hypertext Transfer Protocol (HTTP) is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenablemulticast">GetEnableMulticast</a>
</td>
<td align="left" width="63%">
Ascertains whether multicast is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenabletcp">GetEnableTCP</a>
</td>
<td align="left" width="63%">
Ascertains whether TCP is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenableudp">GetEnableUDP</a>
</td>
<td align="left" width="63%">
Ascertains whether <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">UDP</a> is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getforcererunautoproxydetection">GetForceRerunAutoProxyDetection</a>
</td>
<td align="left" width="63%">
Ascertains whether forced rerun detection is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getloggingurl">GetLoggingUrl</a>
</td>
<td align="left" width="63%">
Retrieves the URL corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getloggingurlcount">GetLoggingUrlCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of URLs in the current list of logging URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getnumprotocolssupported">GetNumProtocolsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the number of supported protocols.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxybypassforlocal">GetProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Retrieves the configuration setting for bypassing the proxy for local hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxyexceptionlist">GetProxyExceptionList</a>
</td>
<td align="left" width="63%">
Retrieves the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxyhostname">GetProxyHostName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the host to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxyport">GetProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the port to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxysettings">GetProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the current proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname">GetSupportedProtocolName</a>
</td>
<td align="left" width="63%">
Retrieves a protocol name by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getudpportranges">GetUDPPortRanges</a>
</td>
<td align="left" width="63%">
Retrieves the UDP port number ranges that are used for receiving data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist">ResetLoggingUrlList</a>
</td>
<td align="left" width="63%">
Clears the list of logging URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetprotocolrollover">ResetProtocolRollover</a>
</td>
<td align="left" width="63%">
Forces the reader object to use the normal protocol rollover algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setbufferingtime">SetBufferingTime</a>
</td>
<td align="left" width="63%">
Specifies how long the network source buffers data before rendering it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth">SetConnectionBandwidth</a>
</td>
<td align="left" width="63%">
Specifies the connection bandwidth for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenablehttp">SetEnableHTTP</a>
</td>
<td align="left" width="63%">
Enables or disables HTTP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenablemulticast">SetEnableMulticast</a>
</td>
<td align="left" width="63%">
Enables or disables multicast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp">SetEnableTCP</a>
</td>
<td align="left" width="63%">
Enables or disables TCP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp">SetEnableUDP</a>
</td>
<td align="left" width="63%">
Enables or disables UDP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setforcererunautoproxydetection">SetForceRerunAutoProxyDetection</a>
</td>
<td align="left" width="63%">
Enables or disables forced rerun detection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxybypassforlocal">SetProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Specifies the configuration setting for bypassing the proxy for local hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyexceptionlist">SetProxyExceptionList</a>
</td>
<td align="left" width="63%">
Specifies the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyhostname">SetProxyHostName</a>
</td>
<td align="left" width="63%">
Specifies the name of the host to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyport">SetProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the port to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxysettings">SetProxySettings</a>
</td>
<td align="left" width="63%">
Specifies the proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setudpportranges">SetUDPPortRanges</a>
</td>
<td align="left" width="63%">
Specifies the UDP port number ranges that are used for receiving data.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>
 

 

