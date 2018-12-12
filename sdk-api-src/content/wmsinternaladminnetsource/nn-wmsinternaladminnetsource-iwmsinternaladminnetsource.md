---
UID: NN:wmsinternaladminnetsource.IWMSInternalAdminNetSource
title: IWMSInternalAdminNetSource
author: windows-sdk-content
description: The IWMSInternalAdminNetSource interface manages cached passwords and finds proxy servers.To obtain a pointer to an instance of this interface, call the QueryInterface method of the IDispatch interface retrieved by INSNetSourceCreator::GetNetSourceAdminInterface.
old-location: wmformat\iwmsinternaladminnetsource.htm
tech.root: wmformat
ms.assetid: 0fbdad85-d94a-4598-bb25-f733df33692a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMSInternalAdminNetSource, IWMSInternalAdminNetSource interface [windows Media Format], IWMSInternalAdminNetSource interface [windows Media Format],described, IWMSInternalAdminNetSourceInterface, wmformat.iwmsinternaladminnetsource, wmsinternaladminnetsource/IWMSInternalAdminNetSource
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMSInternalAdminNetSource
 - IWMSInternalAdminNetSource.GetNetSourceCreator
 - IWMSInternalAdminNetSource.Initialize
 - IWMSInternalAdminNetSource.IsUsingIE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSInternalAdminNetSource interface


## -description



The <b>IWMSInternalAdminNetSource</b> interface manages cached passwords and finds proxy servers.

To obtain a pointer to an instance of this interface, call the <b>QueryInterface</b> method of the <b>IDispatch</b> interface retrieved by <a href="https://msdn.microsoft.com/en-us/library/Dd743240(v=VS.85).aspx">INSNetSourceCreator::GetNetSourceAdminInterface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSInternalAdminNetSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMSInternalAdminNetSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSInternalAdminNetSource</b> interface has these methods.
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798537(v=VS.85).aspx">FindProxyForURL</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name and port number of a proxy server to use for the client.

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
<td align="left" width="37%"><b>GetNetSourceCreator</b></td>
<td align="left" width="63%">
This method is not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>Initialize</b></td>
<td align="left" width="63%">
This method is not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>IsUsingIE</b></td>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798543(v=VS.85).aspx">ShutdownProxyContext</a>
</td>
<td align="left" width="63%">
Releases internally allocated resources used in finding proxy servers.

</td>
</tr>
</table> 


## -remarks



Most of the methods of the <b>IWMSInternalAdminNetSource</b> interface have been updated in <a href="https://msdn.microsoft.com/en-us/library/Dd743718(v=VS.85).aspx">IWMSInternalAdminNetSource2</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd743722(v=VS.85).aspx">IWMSInternalAdminNetSource3</a>. If you are developing an application using a version of the Windows Media Format SDK that supports the later interfaces, you should use them.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743239(v=VS.85).aspx">INSNetSourceCreator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743718(v=VS.85).aspx">IWMSInternalAdminNetSource2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743722(v=VS.85).aspx">IWMSInternalAdminNetSource3 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

