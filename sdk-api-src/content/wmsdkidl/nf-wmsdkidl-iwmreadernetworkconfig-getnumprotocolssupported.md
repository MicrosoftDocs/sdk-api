---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetNumProtocolsSupported
title: IWMReaderNetworkConfig::GetNumProtocolsSupported (wmsdkidl.h)
description: The GetNumProtocolsSupported method retrieves the number of supported protocols.
helpviewer_keywords: ["GetNumProtocolsSupported","GetNumProtocolsSupported method [windows Media Format]","GetNumProtocolsSupported method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetNumProtocolsSupported method","IWMReaderNetworkConfig.GetNumProtocolsSupported","IWMReaderNetworkConfig::GetNumProtocolsSupported","IWMReaderNetworkConfigGetNumProtocolsSupported","wmformat.iwmreadernetworkconfig_getnumprotocolssupported","wmsdkidl/IWMReaderNetworkConfig::GetNumProtocolsSupported"]
old-location: wmformat\iwmreadernetworkconfig_getnumprotocolssupported.htm
tech.root: wmformat
ms.assetid: 6e249d8f-0351-452f-9b53-86f77df2fd70
ms.date: 4/26/2023
ms.keywords: GetNumProtocolsSupported, GetNumProtocolsSupported method [windows Media Format], GetNumProtocolsSupported method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetNumProtocolsSupported method, IWMReaderNetworkConfig.GetNumProtocolsSupported, IWMReaderNetworkConfig::GetNumProtocolsSupported, IWMReaderNetworkConfigGetNumProtocolsSupported, wmformat.iwmreadernetworkconfig_getnumprotocolssupported, wmsdkidl/IWMReaderNetworkConfig::GetNumProtocolsSupported
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
 - IWMReaderNetworkConfig::GetNumProtocolsSupported
 - wmsdkidl/IWMReaderNetworkConfig::GetNumProtocolsSupported
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
 - IWMReaderNetworkConfig.GetNumProtocolsSupported
---

# IWMReaderNetworkConfig::GetNumProtocolsSupported


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetNumProtocolsSupported</b> method retrieves the number of supported protocols.

## -parameters

### -param pcProtocols [out]

Pointer to a count of the protocols.

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

Use this method along with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname">IWMReaderAdvanced2::GetProtocolName</a> to iterate through the network protocols supported by the reader.

This method counts the number of protocols that the reader can use when receiving a stream. It does not indicate the protocols that are available for sending a stream.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>