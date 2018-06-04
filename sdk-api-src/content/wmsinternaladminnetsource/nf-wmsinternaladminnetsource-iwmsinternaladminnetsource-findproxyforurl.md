---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMSInternalAdminNetSource::FindProxyForURL


## -description



The <b>FindProxyForURL</b> method finds a proxy server name and port to use for the client.




## -parameters




### -param bstrProtocol [in]

String containing the protocol for which to find the proxy server. Typically, this is either "http" or "mms".


### -param bstrHost [in]

String containing the DNS name or IP address of the server with which you want to communicate. Depending upon the server, the proxy might be different.


### -param pfProxyEnabled [out]

Pointer to a Boolean value that is True if the user has enabled a proxy that applies to the specified protocol and host.


### -param pbstrProxyServer [out]

Pointer to a string containing the proxy server DNS name.


### -param pdwProxyPort [out]

Pointer to a <b>DWORD</b> containing the proxy port number.


### -param pdwProxyContext [in, out]

<b>DWORD</b> representing the proxy server returned. You can make multiple calls to <b>FindProxyForURL</b> to find all configured proxy servers. On your first call, set the context to zero. When the call returns, the context is set to a value representing the proxy for which information was returned. On the next call, set the context to the context value retrieved on the first call. Continue this process until the call returns S_FALSE.

This method has internal algorithms that determine how it looks for proxy servers. You can override this and make it find the proxy server set by the client's Web browser, by setting the context to 3.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
When calling this method multiple times to find all proxies configured, this value is returned when there are no more configured proxy servers.

</td>
</tr>
</table>
 




## -remarks



When you have finished making calls to <b>FindProxyForURL</b>, you must call <a href="https://msdn.microsoft.com/95c6f641-e0b1-4391-b4bd-b43c03a330b4">IWMSInternalAdminNetSource::ShutdownProxyContext</a> to free the internal resources used.




## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>
 

 

