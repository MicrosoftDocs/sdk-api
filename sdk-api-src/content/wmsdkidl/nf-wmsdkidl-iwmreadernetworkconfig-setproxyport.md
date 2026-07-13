---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxyPort
title: IWMReaderNetworkConfig::SetProxyPort (wmsdkidl.h)
description: The SetProxyPort method specifies the proxy port.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetProxyPort method","IWMReaderNetworkConfig.SetProxyPort","IWMReaderNetworkConfig::SetProxyPort","IWMReaderNetworkConfigSetProxyPort","SetProxyPort","SetProxyPort method [windows Media Format]","SetProxyPort method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setproxyport","wmsdkidl/IWMReaderNetworkConfig::SetProxyPort"]
old-location: wmformat\iwmreadernetworkconfig_setproxyport.htm
tech.root: wmformat
ms.assetid: e2f4e8ff-6ac8-45b5-af93-a278bf92a07a
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxyPort method, IWMReaderNetworkConfig.SetProxyPort, IWMReaderNetworkConfig::SetProxyPort, IWMReaderNetworkConfigSetProxyPort, SetProxyPort, SetProxyPort method [windows Media Format], SetProxyPort method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxyport, wmsdkidl/IWMReaderNetworkConfig::SetProxyPort
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
 - IWMReaderNetworkConfig::SetProxyPort
 - wmsdkidl/IWMReaderNetworkConfig::SetProxyPort
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
 - IWMReaderNetworkConfig.SetProxyPort
---

# IWMReaderNetworkConfig::SetProxyPort


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProxyPort</b> method specifies the proxy port.

## -parameters

### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol.

### -param dwPort [in]

<b>DWORD</b> containing the name of the port.

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

By default, the port numbers are 1755 for MMS and 80 for HTTP. The correct port number must be set if a port is required. It is not required if the proxy setting is WMT_PROXY_SETTING_AUTO or WMT_PROXY_SETTING_BROWSER.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxyport">IWMReaderNetworkConfig::GetProxyPort</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxysettings">IWMReaderNetworkConfig::SetProxySettings</a>