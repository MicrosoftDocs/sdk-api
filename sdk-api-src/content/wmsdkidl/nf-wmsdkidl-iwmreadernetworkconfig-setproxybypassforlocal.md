---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxyBypassForLocal
title: IWMReaderNetworkConfig::SetProxyBypassForLocal (wmsdkidl.h)
description: The SetProxyBypassForLocal method specifies the configuration setting for bypassing the proxy for local hosts.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetProxyBypassForLocal method","IWMReaderNetworkConfig.SetProxyBypassForLocal","IWMReaderNetworkConfig::SetProxyBypassForLocal","IWMReaderNetworkConfigSetProxyBypassForLocal","SetProxyBypassForLocal","SetProxyBypassForLocal method [windows Media Format]","SetProxyBypassForLocal method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setproxybypassforlocal","wmsdkidl/IWMReaderNetworkConfig::SetProxyBypassForLocal"]
old-location: wmformat\iwmreadernetworkconfig_setproxybypassforlocal.htm
tech.root: wmformat
ms.assetid: 4a012718-a815-4e01-97f8-69ed2ba881ea
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxyBypassForLocal method, IWMReaderNetworkConfig.SetProxyBypassForLocal, IWMReaderNetworkConfig::SetProxyBypassForLocal, IWMReaderNetworkConfigSetProxyBypassForLocal, SetProxyBypassForLocal, SetProxyBypassForLocal method [windows Media Format], SetProxyBypassForLocal method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxybypassforlocal, wmsdkidl/IWMReaderNetworkConfig::SetProxyBypassForLocal
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
 - IWMReaderNetworkConfig::SetProxyBypassForLocal
 - wmsdkidl/IWMReaderNetworkConfig::SetProxyBypassForLocal
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
 - IWMReaderNetworkConfig.SetProxyBypassForLocal
---

# IWMReaderNetworkConfig::SetProxyBypassForLocal


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProxyBypassForLocal</b> method specifies the configuration setting for bypassing the proxy for local hosts.

## -parameters

### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol.

### -param fBypassForLocal [in]

Boolean value that is True if bypassing the proxy for local hosts is to be enabled (implying that the origin server is on the local network).

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

This setting is used only when the proxy setting is WMT_PROXY_SETTING_MANUAL. If the proxy setting is WMT_PROXY_SETTING_BROWSER, the local bypass flag setting in the browser is used instead.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxybypassforlocal">IWMReaderNetworkConfig::GetProxyBypassForLocal</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxysettings">IWMReaderNetworkConfig::SetProxySettings</a>