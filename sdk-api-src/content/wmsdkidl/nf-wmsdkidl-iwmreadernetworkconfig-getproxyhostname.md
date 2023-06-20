---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyHostName
title: IWMReaderNetworkConfig::GetProxyHostName (wmsdkidl.h)
description: The GetProxyHostName method retrieves the name of the host to use as the proxy.
helpviewer_keywords: ["GetProxyHostName","GetProxyHostName method [windows Media Format]","GetProxyHostName method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetProxyHostName method","IWMReaderNetworkConfig.GetProxyHostName","IWMReaderNetworkConfig::GetProxyHostName","IWMReaderNetworkConfigGetProxyHostName","wmformat.iwmreadernetworkconfig_getproxyhostname","wmsdkidl/IWMReaderNetworkConfig::GetProxyHostName"]
old-location: wmformat\iwmreadernetworkconfig_getproxyhostname.htm
tech.root: wmformat
ms.assetid: a7411ed6-90ee-450c-bb06-408469036d22
ms.date: 4/26/2023
ms.keywords: GetProxyHostName, GetProxyHostName method [windows Media Format], GetProxyHostName method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetProxyHostName method, IWMReaderNetworkConfig.GetProxyHostName, IWMReaderNetworkConfig::GetProxyHostName, IWMReaderNetworkConfigGetProxyHostName, wmformat.iwmreadernetworkconfig_getproxyhostname, wmsdkidl/IWMReaderNetworkConfig::GetProxyHostName
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
 - IWMReaderNetworkConfig::GetProxyHostName
 - wmsdkidl/IWMReaderNetworkConfig::GetProxyHostName
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
 - IWMReaderNetworkConfig.GetProxyHostName
---

# IWMReaderNetworkConfig::GetProxyHostName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetProxyHostName</b> method retrieves the name of the host to use as the proxy.

## -parameters

### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.

### -param pwszHostName [out]

Pointer to a buffer that receives the name of the proxy server host. The returned value applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.

### -param pcchHostName [in, out]

On input, pointer to a variable specifying the size of <i>pwszHostName</i>, in characters. On output, the variable contains the length of the string, including the terminating <b>null</b> character.

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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size of the buffer passed in is not large enough to hold the return string.

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
</table>

## -remarks

Call this method twice. The first time, pass <b>NULL</b> as the value for <i>pwszHostName</i>. The method returns the size of the string in the <i>pcchHostName</i> parameter. Allocate the required amount of memory for the string and call the method again. This time, pass a pointer to the allocated buffer in the <i>pwszHostName</i> parameter.

The host name is ignored if the proxy setting is WMT_PROXY_SETTING_AUTO or WMT_PROXY_SETTING_BROWSER.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyhostname">IWMReaderNetworkConfig::SetProxyHostName</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxysettings">IWMReaderNetworkConfig::SetProxySettings</a>