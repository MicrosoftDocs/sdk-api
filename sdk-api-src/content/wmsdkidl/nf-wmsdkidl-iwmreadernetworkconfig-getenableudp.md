---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetEnableUDP
title: IWMReaderNetworkConfig::GetEnableUDP (wmsdkidl.h)
description: The GetEnableUDP method queries whether UDP is enabled for protocol rollover.
helpviewer_keywords: ["GetEnableUDP","GetEnableUDP method [windows Media Format]","GetEnableUDP method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetEnableUDP method","IWMReaderNetworkConfig.GetEnableUDP","IWMReaderNetworkConfig::GetEnableUDP","IWMReaderNetworkConfigGetEnableUDP","wmformat.iwmreadernetworkconfig_getenableudp","wmsdkidl/IWMReaderNetworkConfig::GetEnableUDP"]
old-location: wmformat\iwmreadernetworkconfig_getenableudp.htm
tech.root: wmformat
ms.assetid: 81c6536c-303c-4eac-a75a-54e9df29e299
ms.date: 4/26/2023
ms.keywords: GetEnableUDP, GetEnableUDP method [windows Media Format], GetEnableUDP method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetEnableUDP method, IWMReaderNetworkConfig.GetEnableUDP, IWMReaderNetworkConfig::GetEnableUDP, IWMReaderNetworkConfigGetEnableUDP, wmformat.iwmreadernetworkconfig_getenableudp, wmsdkidl/IWMReaderNetworkConfig::GetEnableUDP
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
 - IWMReaderNetworkConfig::GetEnableUDP
 - wmsdkidl/IWMReaderNetworkConfig::GetEnableUDP
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
 - IWMReaderNetworkConfig.GetEnableUDP
---

# IWMReaderNetworkConfig::GetEnableUDP


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetEnableUDP</b> method queries whether <a href="/windows/desktop/wmformat/wmformat-glossary">UDP</a> is enabled for protocol rollover.

## -parameters

### -param pfEnableUDP [out]

Pointer to a variable that receives a Boolean value. If the value is <b>TRUE</b>, the reader object includes UDP when it performs protocol rollover. If the value is <b>FALSE</b>, the reader does not use UDP for protocol rollover. However, the reader will still use UDP if the URL explicitly specifies a UDP-based protocol, such as MMSU or RTSPU.

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

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenabletcp">IWMReaderNetworkConfig::GetEnableTCP</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp">IWMReaderNetworkConfig::SetEnableTCP</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp">IWMReaderNetworkConfig::SetEnableUDP</a>