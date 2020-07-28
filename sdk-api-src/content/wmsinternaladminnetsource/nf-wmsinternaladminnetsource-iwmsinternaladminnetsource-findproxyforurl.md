---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.FindProxyForURL
title: IWMSInternalAdminNetSource::FindProxyForURL (wmsinternaladminnetsource.h)
description: The FindProxyForURL method finds a proxy server name and port to use for the client.
helpviewer_keywords: ["FindProxyForURL","FindProxyForURL method [windows Media Format]","FindProxyForURL method [windows Media Format]","IWMSInternalAdminNetSource interface","IWMSInternalAdminNetSource interface [windows Media Format]","FindProxyForURL method","IWMSInternalAdminNetSource.FindProxyForURL","IWMSInternalAdminNetSource::FindProxyForURL","IWMSInternalAdminNetSourceFindProxyForURL","wmformat.iwmsinternaladminnetsource_findproxyforurl","wmsinternaladminnetsource/IWMSInternalAdminNetSource::FindProxyForURL"]
old-location: wmformat\iwmsinternaladminnetsource_findproxyforurl.htm
tech.root: wmformat
ms.assetid: 5c05ed2b-98ff-417c-bc48-4e8a3dd95460
ms.date: 12/05/2018
ms.keywords: FindProxyForURL, FindProxyForURL method [windows Media Format], FindProxyForURL method [windows Media Format],IWMSInternalAdminNetSource interface, IWMSInternalAdminNetSource interface [windows Media Format],FindProxyForURL method, IWMSInternalAdminNetSource.FindProxyForURL, IWMSInternalAdminNetSource::FindProxyForURL, IWMSInternalAdminNetSourceFindProxyForURL, wmformat.iwmsinternaladminnetsource_findproxyforurl, wmsinternaladminnetsource/IWMSInternalAdminNetSource::FindProxyForURL
f1_keywords:
- wmsinternaladminnetsource/IWMSInternalAdminNetSource.FindProxyForURL
dev_langs:
- c++
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMSInternalAdminNetSource.FindProxyForURL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



When you have finished making calls to <b>FindProxyForURL</b>, you must call <a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-shutdownproxycontext">IWMSInternalAdminNetSource::ShutdownProxyContext</a> to free the internal resources used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>
 

 

