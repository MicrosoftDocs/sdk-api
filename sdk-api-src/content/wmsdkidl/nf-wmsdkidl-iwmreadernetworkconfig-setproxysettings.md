---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxySettings
title: IWMReaderNetworkConfig::SetProxySettings (wmsdkidl.h)
description: The SetProxySettings method specifies the proxy settings.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetProxySettings method","IWMReaderNetworkConfig.SetProxySettings","IWMReaderNetworkConfig::SetProxySettings","IWMReaderNetworkConfigSetProxySettings","SetProxySettings","SetProxySettings method [windows Media Format]","SetProxySettings method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setproxysettings","wmsdkidl/IWMReaderNetworkConfig::SetProxySettings"]
old-location: wmformat\iwmreadernetworkconfig_setproxysettings.htm
tech.root: wmformat
ms.assetid: fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxySettings method, IWMReaderNetworkConfig.SetProxySettings, IWMReaderNetworkConfig::SetProxySettings, IWMReaderNetworkConfigSetProxySettings, SetProxySettings, SetProxySettings method [windows Media Format], SetProxySettings method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxysettings, wmsdkidl/IWMReaderNetworkConfig::SetProxySettings
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
 - IWMReaderNetworkConfig::SetProxySettings
 - wmsdkidl/IWMReaderNetworkConfig::SetProxySettings
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
 - IWMReaderNetworkConfig.SetProxySettings
---

# IWMReaderNetworkConfig::SetProxySettings


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProxySettings</b> method specifies the proxy settings.

## -parameters

### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol name. Supported names are HTTP and MMS.

### -param ProxySetting [in]

A value from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_proxy_settings">WMT_PROXY_SETTINGS</a> enumeration type.

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
NULL or invalid argument passed in.

</td>
</tr>
</table>

## -remarks

Setting the protocol to WMT_PROXY_SETTING_MANUAL causes the reader to use the proxy settings from <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyhostname">SetProxyHostName</a> and <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyport">SetProxyPort</a>. Setting it to WMT_PROXY_SETTING_AUTO uses Web Proxy Auto-Detect mechanisms to dynamically determine the appropriate proxy based on the specified URL. Setting the protocol to WMT_PROXY_SETTING_BROWSER is valid only for HTTP URLs, and causes the reader to use the proxy settings that are configured in the browser.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxysettings">IWMReaderNetworkConfig::GetProxySettings</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyhostname">IWMReaderNetworkConfig::SetProxyHostName</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyport">IWMReaderNetworkConfig::SetProxyPort</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_proxy_settings">WMT_PROXY_SETTINGS</a>