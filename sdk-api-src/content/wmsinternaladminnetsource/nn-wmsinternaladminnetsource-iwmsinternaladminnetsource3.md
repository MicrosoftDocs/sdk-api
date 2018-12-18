---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource3
title: IWMSInternalAdminNetSource3
author: windows-sdk-content
description: The IWMSInternalAdminNetSource3 interface provides improved methods to find proxy servers.To obtain a pointer to an instance of this interface, call the QueryInterface method of the IDispatch method retrieved by INSNetSourceCreator::GetNetSourceAdminInterface.
old-location: wmformat\iwmsinternaladminnetsource3.htm
tech.root: wmformat
ms.assetid: b4ca08a4-6e2d-4646-b101-67bac67300b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMSInternalAdminNetSource3, IWMSInternalAdminNetSource3 interface [windows Media Format], IWMSInternalAdminNetSource3 interface [windows Media Format],described, IWMSInternalAdminNetSource3Interface, wmformat.iwmsinternaladminnetsource3, wmsinternaladminnetsource/IWMSInternalAdminNetSource3
ms.topic: interface
req.header: wmsinternaladminnetsource.h
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
 - wmsinternaladminnetsource.h
api_name:
 - IWMSInternalAdminNetSource3
 - IWMSInternalAdminNetSource3.GetNetSourceCreator2
 - IWMSInternalAdminNetSource3.IsUsingIE2
 - IWMSInternalAdminNetSource3.RegisterProxyFailure2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSInternalAdminNetSource3 interface


## -description



The <b>IWMSInternalAdminNetSource3</b> interface provides improved methods to find proxy servers.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> method retrieved by <a href="https://msdn.microsoft.com/en-us/library/Dd743240(v=VS.85).aspx">INSNetSourceCreator::GetNetSourceAdminInterface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSInternalAdminNetSource3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd743718(v=VS.85).aspx">IWMSInternalAdminNetSource2</a>. <b>IWMSInternalAdminNetSource3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSInternalAdminNetSource3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798536(v=VS.85).aspx">DeleteCredentials</a>
</td>
<td align="left" width="63%">
Removes a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743719(v=VS.85).aspx">DeleteCredentialsEx</a>
</td>
<td align="left" width="63%">
Removes a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798537(v=VS.85).aspx">FindProxyForURL</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name and port number of a proxy server that should be used for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743723(v=VS.85).aspx">FindProxyForURLEx2</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name and port number of a proxy server that should be used for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798538(v=VS.85).aspx">GetCredentialFlags</a>
</td>
<td align="left" width="63%">
Retrieves the user's preference for password caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798539(v=VS.85).aspx">GetCredentials</a>
</td>
<td align="left" width="63%">
Retrieves a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743720(v=VS.85).aspx">GetCredentialsEx</a>
</td>
<td align="left" width="63%">
Retrieves a cached password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743724(v=VS.85).aspx">GetCredentialsEx2</a>
</td>
<td align="left" width="63%">
Retrieves a cached password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetNetSourceCreator2</b></td>
<td align="left" width="63%">
This method is not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>IsUsingIE2</b></td>
<td align="left" width="63%">
This method is not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798540(v=VS.85).aspx">RegisterProxyFailure</a>
</td>
<td align="left" width="63%">
Registers a proxy failure.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>RegisterProxyFailure2</b></td>
<td align="left" width="63%">
This method is not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798541(v=VS.85).aspx">SetCredentialFlags</a>
</td>
<td align="left" width="63%">
Sets the user's preference for password caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798542(v=VS.85).aspx">SetCredentials</a>
</td>
<td align="left" width="63%">
Saves a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743721(v=VS.85).aspx">SetCredentialsEx</a>
</td>
<td align="left" width="63%">
Saves a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798534(v=VS.85).aspx">SetCredentialsEx2</a>
</td>
<td align="left" width="63%">
Adds a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798543(v=VS.85).aspx">ShutdownProxyContext</a>
</td>
<td align="left" width="63%">
Releases internally allocated resources used in finding proxy servers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798535(v=VS.85).aspx">ShutdownProxyContext2</a>
</td>
<td align="left" width="63%">
Releases internally allocated resources used in finding proxy servers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743717(v=VS.85).aspx">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743718(v=VS.85).aspx">IWMSInternalAdminNetSource2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

