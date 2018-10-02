---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource2
title: IWMSInternalAdminNetSource2
author: windows-sdk-content
description: The IWMSInternalAdminNetSource2 interface provides improved methods for password caching.
old-location: wmformat\iwmsinternaladminnetsource2.htm
tech.root: wmformat
ms.assetid: 6d334725-11d5-4249-a83d-fc8c1c35a56f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMSInternalAdminNetSource2, IWMSInternalAdminNetSource2 interface [windows Media Format], IWMSInternalAdminNetSource2 interface [windows Media Format],described, IWMSInternalAdminNetSource2Interface, wmformat.iwmsinternaladminnetsource2, wmsinternaladminnetsource/IWMSInternalAdminNetSource2
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMSInternalAdminNetSource2
 - IWMSInternalAdminNetSource2.FindProxyForURLEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSInternalAdminNetSource2 interface


## -description



The <b>IWMSInternalAdminNetSource2</b> interface provides improved methods for password caching. These methods should be used in preference to their counterparts in <a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource</a> because the older methods are vulnerable to spoofing and are therefore not secure.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> method retrieved by <a href="https://msdn.microsoft.com/147b431f-84ed-40b9-85a8-3c220b56cd3f">INSNetSourceCreator::GetNetSourceAdminInterface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSInternalAdminNetSource2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMSInternalAdminNetSource2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSInternalAdminNetSource2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16144c10-419c-4e6a-bc96-2f429c793257">DeleteCredentials</a>
</td>
<td align="left" width="63%">
Removes a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06d82f1d-b965-40fb-8a79-904ba5af7191">DeleteCredentialsEx</a>
</td>
<td align="left" width="63%">
Removes a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c05ed2b-98ff-417c-bc48-4e8a3dd95460">FindProxyForURL</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name and port number of a proxy server that should be used for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>FindProxyForURLEx</b></td>
<td align="left" width="63%">
This method is not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/781b2868-c8e2-4d92-98f2-c2950fac3d9b">GetCredentialFlags</a>
</td>
<td align="left" width="63%">
Retrieves the user's preference for password caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4d6bcc3-a32b-4270-8b43-f3b6a5046fd6">GetCredentials</a>
</td>
<td align="left" width="63%">
Retrieves a password from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5840fe0b-34f6-4e39-b55f-7e07b7795e52">GetCredentialsEx</a>
</td>
<td align="left" width="63%">
Retrieves a cached password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50a41a98-2827-425e-91fc-5196996abe98">RegisterProxyFailure</a>
</td>
<td align="left" width="63%">
Registers a proxy failure.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af6208b3-84f6-44d1-9587-140044f2b2f0">SetCredentialFlags</a>
</td>
<td align="left" width="63%">
Sets the user's preference for password caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0655ed3-8d14-447a-b74f-054498eb75e9">SetCredentials</a>
</td>
<td align="left" width="63%">
Saves a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca45626e-3f4d-415d-a4d1-90ce0177bd10">SetCredentialsEx</a>
</td>
<td align="left" width="63%">
Saves a password to the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c6f641-e0b1-4391-b4bd-b43c03a330b4">ShutdownProxyContext</a>
</td>
<td align="left" width="63%">
Releases internally allocated resources used in finding proxy servers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/b4ca08a4-6e2d-4646-b101-67bac67300b1">IWMSInternalAdminNetSource3 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

