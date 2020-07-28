---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource3
title: IWMSInternalAdminNetSource3 (wmsinternaladminnetsource.h)
description: The IWMSInternalAdminNetSource3 interface provides improved methods to find proxy servers.To obtain a pointer to an instance of this interface, call the QueryInterface method of the IDispatch method retrieved by INSNetSourceCreator::GetNetSourceAdminInterface.
helpviewer_keywords: ["IWMSInternalAdminNetSource3","IWMSInternalAdminNetSource3 interface [windows Media Format]","IWMSInternalAdminNetSource3 interface [windows Media Format]","described","IWMSInternalAdminNetSource3Interface","wmformat.iwmsinternaladminnetsource3","wmsinternaladminnetsource/IWMSInternalAdminNetSource3"]
old-location: wmformat\iwmsinternaladminnetsource3.htm
tech.root: wmformat
ms.assetid: b4ca08a4-6e2d-4646-b101-67bac67300b1
ms.date: 12/05/2018
ms.keywords: IWMSInternalAdminNetSource3, IWMSInternalAdminNetSource3 interface [windows Media Format], IWMSInternalAdminNetSource3 interface [windows Media Format],described, IWMSInternalAdminNetSource3Interface, wmformat.iwmsinternaladminnetsource3, wmsinternaladminnetsource/IWMSInternalAdminNetSource3
f1_keywords:
- wmsinternaladminnetsource/IWMSInternalAdminNetSource3
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSInternalAdminNetSource3 interface


## -description



The <b>IWMSInternalAdminNetSource3</b> interface provides improved methods to find proxy servers.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> method retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-getnetsourceadmininterface">INSNetSourceCreator::GetNetSourceAdminInterface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSInternalAdminNetSource3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2</a>. <b>IWMSInternalAdminNetSource3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-deletecredentials">DeleteCredentials</a>
</td>
<td align="left" width="63%">
Removes a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-deletecredentialsex">DeleteCredentialsEx</a>
</td>
<td align="left" width="63%">
Removes a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-findproxyforurl">FindProxyForURL</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name and port number of a proxy server that should be used for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-findproxyforurlex2">FindProxyForURLEx2</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name and port number of a proxy server that should be used for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-getcredentialflags">GetCredentialFlags</a>
</td>
<td align="left" width="63%">
Retrieves the user's preference for password caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-getcredentials">GetCredentials</a>
</td>
<td align="left" width="63%">
Retrieves a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-getcredentialsex">GetCredentialsEx</a>
</td>
<td align="left" width="63%">
Retrieves a cached password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-getcredentialsex2">GetCredentialsEx2</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-registerproxyfailure">RegisterProxyFailure</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-setcredentialflags">SetCredentialFlags</a>
</td>
<td align="left" width="63%">
Sets the user's preference for password caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-setcredentials">SetCredentials</a>
</td>
<td align="left" width="63%">
Saves a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-setcredentialsex">SetCredentialsEx</a>
</td>
<td align="left" width="63%">
Saves a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-setcredentialsex2">SetCredentialsEx2</a>
</td>
<td align="left" width="63%">
Adds a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-shutdownproxycontext">ShutdownProxyContext</a>
</td>
<td align="left" width="63%">
Releases internally allocated resources used in finding proxy servers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-shutdownproxycontext2">ShutdownProxyContext2</a>
</td>
<td align="left" width="63%">
Releases internally allocated resources used in finding proxy servers.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

