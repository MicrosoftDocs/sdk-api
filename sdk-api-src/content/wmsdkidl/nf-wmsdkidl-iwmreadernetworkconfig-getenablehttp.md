---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetEnableHTTP
title: IWMReaderNetworkConfig::GetEnableHTTP (wmsdkidl.h)
description: The GetEnableHTTP method queries whether HTTP is enabled for protocol rollover.
helpviewer_keywords: ["GetEnableHTTP","GetEnableHTTP method [windows Media Format]","GetEnableHTTP method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetEnableHTTP method","IWMReaderNetworkConfig.GetEnableHTTP","IWMReaderNetworkConfig::GetEnableHTTP","IWMReaderNetworkConfigGetEnableHTTP","wmformat.iwmreadernetworkconfig_getenablehttp","wmsdkidl/IWMReaderNetworkConfig::GetEnableHTTP"]
old-location: wmformat\iwmreadernetworkconfig_getenablehttp.htm
tech.root: wmformat
ms.assetid: 892879a3-8ab2-4d2c-ba47-9f6c2dd2aec3
ms.date: 4/26/2023
ms.keywords: GetEnableHTTP, GetEnableHTTP method [windows Media Format], GetEnableHTTP method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetEnableHTTP method, IWMReaderNetworkConfig.GetEnableHTTP, IWMReaderNetworkConfig::GetEnableHTTP, IWMReaderNetworkConfigGetEnableHTTP, wmformat.iwmreadernetworkconfig_getenablehttp, wmsdkidl/IWMReaderNetworkConfig::GetEnableHTTP
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
 - IWMReaderNetworkConfig::GetEnableHTTP
 - wmsdkidl/IWMReaderNetworkConfig::GetEnableHTTP
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
 - IWMReaderNetworkConfig.GetEnableHTTP
---

# IWMReaderNetworkConfig::GetEnableHTTP


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetEnableHTTP</b> method queries whether HTTP is enabled for protocol rollover.

## -parameters

### -param pfEnableHTTP [out]

Pointer to a variable that receives a Boolean value. If the value is <b>TRUE</b>, the reader object includes HTTP when it performs protocol rollover. If the value is <b>FALSE</b>, the reader does not use HTTP for protocol rollover. However, the reader will still use HTTP if it is explicitly specified in the URL.

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



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenablehttp">IWMReaderNetworkConfig::SetEnableHTTP</a>