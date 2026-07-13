---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyPort
title: IWMReaderNetworkConfig::GetProxyPort (wmsdkidl.h)
description: The GetProxyPort method retrieves the port number of the proxy server.
helpviewer_keywords: ["GetProxyPort","GetProxyPort method [windows Media Format]","GetProxyPort method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetProxyPort method","IWMReaderNetworkConfig.GetProxyPort","IWMReaderNetworkConfig::GetProxyPort","IWMReaderNetworkConfigGetProxyPort","wmformat.iwmreadernetworkconfig_getproxyport","wmsdkidl/IWMReaderNetworkConfig::GetProxyPort"]
old-location: wmformat\iwmreadernetworkconfig_getproxyport.htm
tech.root: wmformat
ms.assetid: 042d702e-b4a1-43f6-b2c4-c81922d7c3f2
ms.date: 4/26/2023
ms.keywords: GetProxyPort, GetProxyPort method [windows Media Format], GetProxyPort method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetProxyPort method, IWMReaderNetworkConfig.GetProxyPort, IWMReaderNetworkConfig::GetProxyPort, IWMReaderNetworkConfigGetProxyPort, wmformat.iwmreadernetworkconfig_getproxyport, wmsdkidl/IWMReaderNetworkConfig::GetProxyPort
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
 - IWMReaderNetworkConfig::GetProxyPort
 - wmsdkidl/IWMReaderNetworkConfig::GetProxyPort
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
 - IWMReaderNetworkConfig.GetProxyPort
---

# IWMReaderNetworkConfig::GetProxyPort


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetProxyPort</b> method retrieves the port number of the proxy server.

## -parameters

### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.

### -param pdwPort [out]

Pointer to a variable that receives the port number. The returned value applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.

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
NULL or invalid argument passed in.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyport">IWMReaderNetworkConfig::SetProxyPort</a>