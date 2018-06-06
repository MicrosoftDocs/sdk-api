---
UID: NN:wmsdkidl.IWMReaderNetworkConfig
title: IWMReaderNetworkConfig
author: windows-sdk-content
description: The IWMReaderNetworkConfig interface is used to set and test network configuration settings.
old-location: wmformat\iwmreadernetworkconfig.htm
old-project: wmformat
ms.assetid: 0957ece7-93fe-411b-b69e-fd03933b09d1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], IWMReaderNetworkConfig interface [windows Media Format],described, IWMReaderNetworkConfigInterface, wmformat.iwmreadernetworkconfig, wmsdkidl/IWMReaderNetworkConfig
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
 - IWMReaderNetworkConfig
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/471b17c8-20e4-44f3-88ee-48a35cd8930c">AddLoggingUrl</a>
</td>
<td align="left" width="63%">
Adds the specified URL to the list of URLs to receive logging data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3f35230-363c-48e7-bef9-b92e0b50b978">GetBufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of time required by the network source to buffer data before rendering it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbbc945d-91ea-4d21-a1ac-2fcbcb081447">GetConnectionBandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the connection bandwidth for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/892879a3-8ab2-4d2c-ba47-9f6c2dd2aec3">GetEnableHTTP</a>
</td>
<td align="left" width="63%">
Ascertains whether Hypertext Transfer Protocol (HTTP) is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fc51a74-18b6-4ddd-9089-9a8bdfce70ea">GetEnableMulticast</a>
</td>
<td align="left" width="63%">
Ascertains whether multicast is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6623c2f9-24cb-4038-9aa5-2eb634b3f1a2">GetEnableTCP</a>
</td>
<td align="left" width="63%">
Ascertains whether TCP is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81c6536c-303c-4eac-a75a-54e9df29e299">GetEnableUDP</a>
</td>
<td align="left" width="63%">
Ascertains whether <a href="wmformat_glossary.htm">UDP</a> is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af4c4f4d-ad19-46b5-b38f-9aa51f2d95ba">GetForceRerunAutoProxyDetection</a>
</td>
<td align="left" width="63%">
Ascertains whether forced rerun detection is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27c5a97b-e04b-4d15-b19a-3c0d78feee95">GetLoggingUrl</a>
</td>
<td align="left" width="63%">
Retrieves the URL corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/869e093f-8936-4b60-8818-ee2c57924d11">GetLoggingUrlCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of URLs in the current list of logging URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e249d8f-0351-452f-9b53-86f77df2fd70">GetNumProtocolsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the number of supported protocols.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e960fa9-d71c-4a13-9210-8a2a86e9989c">GetProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Retrieves the configuration setting for bypassing the proxy for local hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90cf6e58-8666-4bab-974e-a7e999aeddf1">GetProxyExceptionList</a>
</td>
<td align="left" width="63%">
Retrieves the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7411ed6-90ee-450c-bb06-408469036d22">GetProxyHostName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the host to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/042d702e-b4a1-43f6-b2c4-c81922d7c3f2">GetProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the port to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fdfc651-05f5-48b3-aeaf-4557c72bc0c0">GetProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the current proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1047752-c3a2-4555-9dae-ddd91365cd10">GetSupportedProtocolName</a>
</td>
<td align="left" width="63%">
Retrieves a protocol name by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1792fd0-e9c3-4e28-9928-a615e1c9aec8">GetUDPPortRanges</a>
</td>
<td align="left" width="63%">
Retrieves the UDP port number ranges that are used for receiving data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fe71d73-a827-4aed-a37b-db7701cc1180">ResetLoggingUrlList</a>
</td>
<td align="left" width="63%">
Clears the list of logging URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10a11131-48bd-49bd-a767-1c6148f84b95">ResetProtocolRollover</a>
</td>
<td align="left" width="63%">
Forces the reader object to use the normal protocol rollover algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64b8eb13-3b96-4bb7-8d75-0eccb1af5a2f">SetBufferingTime</a>
</td>
<td align="left" width="63%">
Specifies how long the network source buffers data before rendering it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beb84e1b-ebe2-40a0-bcf0-eded9346d7a1">SetConnectionBandwidth</a>
</td>
<td align="left" width="63%">
Specifies the connection bandwidth for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20667a28-e6e0-4ec0-905b-6735291063db">SetEnableHTTP</a>
</td>
<td align="left" width="63%">
Enables or disables HTTP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02e3a7cc-1dcf-4aba-a18f-2056742f0777">SetEnableMulticast</a>
</td>
<td align="left" width="63%">
Enables or disables multicast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8afc62b8-a2f6-4470-8005-804e0980b599">SetEnableTCP</a>
</td>
<td align="left" width="63%">
Enables or disables TCP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03afdef3-2aa8-4826-8dce-6d501fa42bcd">SetEnableUDP</a>
</td>
<td align="left" width="63%">
Enables or disables UDP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c84fc2a-5933-45da-a7a3-728a8837d851">SetForceRerunAutoProxyDetection</a>
</td>
<td align="left" width="63%">
Enables or disables forced rerun detection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a012718-a815-4e01-97f8-69ed2ba881ea">SetProxyBypassForLocal</a>
</td>
<td align="left" width="63%">
Specifies the configuration setting for bypassing the proxy for local hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f6c6bb6-3a42-44da-ab80-e72a19b8d272">SetProxyExceptionList</a>
</td>
<td align="left" width="63%">
Specifies the proxy exception list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5638a5d6-30f3-43eb-b054-cab85948796c">SetProxyHostName</a>
</td>
<td align="left" width="63%">
Specifies the name of the host to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2f4e8ff-6ac8-45b5-af93-a278bf92a07a">SetProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the port to be used as the proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2">SetProxySettings</a>
</td>
<td align="left" width="63%">
Specifies the proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a61943a-8ff9-4504-b76f-25e3c5c8d4a4">SetUDPPortRanges</a>
</td>
<td align="left" width="63%">
Specifies the UDP port number ranges that are used for receiving data.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

