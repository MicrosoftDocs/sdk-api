---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyBypassForLocal
title: IWMReaderNetworkConfig::GetProxyBypassForLocal (wmsdkidl.h)
description: The GetProxyBypassForLocal method queries whether the reader object bypasses the proxy server for local URLs.
helpviewer_keywords: ["GetProxyBypassForLocal","GetProxyBypassForLocal method [windows Media Format]","GetProxyBypassForLocal method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetProxyBypassForLocal method","IWMReaderNetworkConfig.GetProxyBypassForLocal","IWMReaderNetworkConfig::GetProxyBypassForLocal","IWMReaderNetworkConfigGetProxyBypassForLocal","wmformat.iwmreadernetworkconfig_getproxybypassforlocal","wmsdkidl/IWMReaderNetworkConfig::GetProxyBypassForLocal"]
old-location: wmformat\iwmreadernetworkconfig_getproxybypassforlocal.htm
tech.root: wmformat
ms.assetid: 5e960fa9-d71c-4a13-9210-8a2a86e9989c
ms.date: 4/26/2023
ms.keywords: GetProxyBypassForLocal, GetProxyBypassForLocal method [windows Media Format], GetProxyBypassForLocal method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetProxyBypassForLocal method, IWMReaderNetworkConfig.GetProxyBypassForLocal, IWMReaderNetworkConfig::GetProxyBypassForLocal, IWMReaderNetworkConfigGetProxyBypassForLocal, wmformat.iwmreadernetworkconfig_getproxybypassforlocal, wmsdkidl/IWMReaderNetworkConfig::GetProxyBypassForLocal
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMReaderNetworkConfig::GetProxyBypassForLocal
 - wmsdkidl/IWMReaderNetworkConfig::GetProxyBypassForLocal
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
 - IWMReaderNetworkConfig.GetProxyBypassForLocal
---

# IWMReaderNetworkConfig::GetProxyBypassForLocal


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetProxyBypassForLocal</b> method queries whether the reader object bypasses the proxy server for local URLs.

## -parameters

### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.

### -param pfBypassForLocal [out]

Pointer to a variable that receives a Boolean value. If the value is <b>TRUE</b>, the reader bypasses the proxy server when it retrieves a URL from a local host. If the value is <b>FALSE</b>, the reader always goes through the proxy server (if any). The returned value applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> or invalid argument passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete task

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxybypassforlocal">IWMReaderNetworkConfig::SetProxyBypassForLocal</a>