---
UID: NN:wmsdkidl.IWMReaderNetworkConfig
title: IWMReaderNetworkConfig
author: windows-sdk-content
description: The IWMReaderNetworkConfig interface is used to set and test network configuration settings.
old-location: wmformat\iwmreadernetworkconfig.htm
tech.root: wmformat
ms.assetid: 0957ece7-93fe-411b-b69e-fd03933b09d1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], IWMReaderNetworkConfig interface [windows Media Format],described, IWMReaderNetworkConfigInterface, wmformat.iwmreadernetworkconfig, wmsdkidl/IWMReaderNetworkConfig
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
 - IWMReaderNetworkConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig interface


## -description



The <b>IWMReaderNetworkConfig</b> interface is used to set and test network configuration settings. By using this interface, the application can configure which protocols must be used to receive the stream as well as other advanced network settings, such as proxy specification and buffering time.

An <b>IWMReaderNetworkConfig</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderNetworkConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderNetworkConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743519(v=VS.85).aspx">AddLoggingUrl</a>
</td>
<td align="left" width="63%">
Adds the specified URL to the list of URLs to receive logging data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743520(v=VS.85).aspx">GetBufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of time required by the network source to buffer data before rendering it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743521(v=VS.85).aspx">GetConnectionBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the connection bandwidth for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743522(v=VS.85).aspx">GetEnableHTTP</a>
</td>
<td align="left" width="63%">
Ascertains whether Hypertext Transfer Protocol (HTTP) is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743523(v=VS.85).aspx">GetEnableMulticast</a>
</td>
<td align="left" width="63%">
Ascertains whether multicast is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743524(v=VS.85).aspx">GetEnableTCP</a>
</td>
<td align="left" width="63%">
Ascertains whether TCP is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743525(v=VS.85).aspx">GetEnableUDP</a>
</td>
<td align="left" width="63%">
Ascertains whether <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">UDP</a> is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743526(v=VS.85).aspx">GetForceRerunAutoProxyDetection</a>
</td>
<td align="left" width="63%">
Ascertains whether forced rerun detection is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743527(v=VS.85).aspx">GetLoggingUrl</a>
</td>
<td align="left" width="63%">
Retrieves the URL corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743528(v=VS.85).aspx">GetLoggingUrlCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of URLs in the current list of logging URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743529(v=VS.85).aspx">GetNumProtocolsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the number of supported protocols.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743530(v=VS.85).aspx">GetProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Retrieves the configuration setting for bypassing the proxy for local hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743531(v=VS.85).aspx">GetProxyExceptionList</a>
</td>
<td align="left" width="63%">
Retrieves the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743532(v=VS.85).aspx">GetProxyHostName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the host to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743533(v=VS.85).aspx">GetProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the port to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743534(v=VS.85).aspx">GetProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the current proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743535(v=VS.85).aspx">GetSupportedProtocolName</a>
</td>
<td align="left" width="63%">
Retrieves a protocol name by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743536(v=VS.85).aspx">GetUDPPortRanges</a>
</td>
<td align="left" width="63%">
Retrieves the UDP port number ranges that are used for receiving data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743537(v=VS.85).aspx">ResetLoggingUrlList</a>
</td>
<td align="left" width="63%">
Clears the list of logging URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743538(v=VS.85).aspx">ResetProtocolRollover</a>
</td>
<td align="left" width="63%">
Forces the reader object to use the normal protocol rollover algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743539(v=VS.85).aspx">SetBufferingTime</a>
</td>
<td align="left" width="63%">
Specifies how long the network source buffers data before rendering it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743540(v=VS.85).aspx">SetConnectionBandwidth</a>
</td>
<td align="left" width="63%">
Specifies the connection bandwidth for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743541(v=VS.85).aspx">SetEnableHTTP</a>
</td>
<td align="left" width="63%">
Enables or disables HTTP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743542(v=VS.85).aspx">SetEnableMulticast</a>
</td>
<td align="left" width="63%">
Enables or disables multicast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743543(v=VS.85).aspx">SetEnableTCP</a>
</td>
<td align="left" width="63%">
Enables or disables TCP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743544(v=VS.85).aspx">SetEnableUDP</a>
</td>
<td align="left" width="63%">
Enables or disables UDP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743545(v=VS.85).aspx">SetForceRerunAutoProxyDetection</a>
</td>
<td align="left" width="63%">
Enables or disables forced rerun detection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743546(v=VS.85).aspx">SetProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Specifies the configuration setting for bypassing the proxy for local hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743547(v=VS.85).aspx">SetProxyExceptionList</a>
</td>
<td align="left" width="63%">
Specifies the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743548(v=VS.85).aspx">SetProxyHostName</a>
</td>
<td align="left" width="63%">
Specifies the name of the host to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743549(v=VS.85).aspx">SetProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the port to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743550(v=VS.85).aspx">SetProxySettings</a>
</td>
<td align="left" width="63%">
Specifies the proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743551(v=VS.85).aspx">SetUDPPortRanges</a>
</td>
<td align="left" width="63%">
Specifies the UDP port number ranges that are used for receiving data.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

