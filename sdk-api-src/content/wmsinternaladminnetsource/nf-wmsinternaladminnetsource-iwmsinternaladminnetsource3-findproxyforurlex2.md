---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource3.FindProxyForURLEx2
title: IWMSInternalAdminNetSource3::FindProxyForURLEx2 (wmsinternaladminnetsource.h)
description: The FindProxyForURLEx2 method finds a proxy server name and port to use for the user.
helpviewer_keywords: ["FindProxyForURLEx2","FindProxyForURLEx2 method [windows Media Format]","FindProxyForURLEx2 method [windows Media Format]","IWMSInternalAdminNetSource3 interface","IWMSInternalAdminNetSource3 interface [windows Media Format]","FindProxyForURLEx2 method","IWMSInternalAdminNetSource3.FindProxyForURLEx2","IWMSInternalAdminNetSource3::FindProxyForURLEx2","IWMSInternalAdminNetSource3FindProxyForURLEx2","wmformat.iwmsinternaladminnetsource3_findproxyforurlex2","wmsinternaladminnetsource/IWMSInternalAdminNetSource3::FindProxyForURLEx2"]
old-location: wmformat\iwmsinternaladminnetsource3_findproxyforurlex2.htm
tech.root: wmformat
ms.assetid: 03c52ed2-bf77-4013-89d6-544d048f1056
ms.date: 4/26/2023
ms.keywords: FindProxyForURLEx2, FindProxyForURLEx2 method [windows Media Format], FindProxyForURLEx2 method [windows Media Format],IWMSInternalAdminNetSource3 interface, IWMSInternalAdminNetSource3 interface [windows Media Format],FindProxyForURLEx2 method, IWMSInternalAdminNetSource3.FindProxyForURLEx2, IWMSInternalAdminNetSource3::FindProxyForURLEx2, IWMSInternalAdminNetSource3FindProxyForURLEx2, wmformat.iwmsinternaladminnetsource3_findproxyforurlex2, wmsinternaladminnetsource/IWMSInternalAdminNetSource3::FindProxyForURLEx2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSInternalAdminNetSource3::FindProxyForURLEx2
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource3::FindProxyForURLEx2
dev_langs:
 - c++
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
 - IWMSInternalAdminNetSource3.FindProxyForURLEx2
---

# IWMSInternalAdminNetSource3::FindProxyForURLEx2


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>FindProxyForURLEx2</b> method finds a proxy server name and port to use for the user.

## -parameters

### -param bstrProtocol [in]

String containing the protocol for which to find the proxy server. Typically, this is either "http" or "mms".

### -param bstrHost [in]

String containing the DNS name, or IP address, of the server with which you want to communicate. Depending upon the server, the proxy might be different.

### -param bstrUrl [in]

String containing the full URL of the site to which you want to connect.

### -param pfProxyEnabled [out]

Pointer to a Boolean value that is set to True if the user has enabled a proxy that applies to the specified protocol, host, and site.

### -param pbstrProxyServer [out]

Pointer to a string containing the proxy server DNS name.

### -param pdwProxyPort [out]

Pointer to a <b>DWORD</b> containing the proxy port number.

### -param pqwProxyContext [in, out]

<b>QWORD</b> representing the proxy server returned. You can make multiple calls to <b>FindProxyForURL</b> to find all configured proxy servers. On your first call, set the context to zero. When the call returns, the context is set to a value representing the proxy for which information was returned. On the next call, set the context to the context value retrieved on the first call. Continue this process until the call returns S_FALSE.

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

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource3">IWMSInternalAdminNetSource3 Interface</a>