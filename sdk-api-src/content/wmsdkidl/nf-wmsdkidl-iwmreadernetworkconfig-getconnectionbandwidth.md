---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetConnectionBandwidth
title: IWMReaderNetworkConfig::GetConnectionBandwidth (wmsdkidl.h)
description: The GetConnectionBandwidth method retrieves the connection bandwidth for the client.
helpviewer_keywords: ["GetConnectionBandwidth","GetConnectionBandwidth method [windows Media Format]","GetConnectionBandwidth method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetConnectionBandwidth method","IWMReaderNetworkConfig.GetConnectionBandwidth","IWMReaderNetworkConfig::GetConnectionBandwidth","IWMReaderNetworkConfigGetConnectionBandwidth","wmformat.iwmreadernetworkconfig_getconnectionbandwidth","wmsdkidl/IWMReaderNetworkConfig::GetConnectionBandwidth"]
old-location: wmformat\iwmreadernetworkconfig_getconnectionbandwidth.htm
tech.root: wmformat
ms.assetid: cbbc945d-91ea-4d21-a1ac-2fcbcb081447
ms.date: 4/26/2023
ms.keywords: GetConnectionBandwidth, GetConnectionBandwidth method [windows Media Format], GetConnectionBandwidth method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetConnectionBandwidth method, IWMReaderNetworkConfig.GetConnectionBandwidth, IWMReaderNetworkConfig::GetConnectionBandwidth, IWMReaderNetworkConfigGetConnectionBandwidth, wmformat.iwmreadernetworkconfig_getconnectionbandwidth, wmsdkidl/IWMReaderNetworkConfig::GetConnectionBandwidth
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
 - IWMReaderNetworkConfig::GetConnectionBandwidth
 - wmsdkidl/IWMReaderNetworkConfig::GetConnectionBandwidth
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
 - IWMReaderNetworkConfig.GetConnectionBandwidth
---

# IWMReaderNetworkConfig::GetConnectionBandwidth


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetConnectionBandwidth</b> method retrieves the connection bandwidth for the client.

## -parameters

### -param pdwConnectionBandwidth [out]

Pointer to a <b>DWORD</b> containing the connection bandwidth, in bits per second.

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

If this method returns zero, the bandwidth could not be detected. If the application has not called <b>SetConnectionBandwidth</b> (or called it with a zero parameter), the return value is the connection rate detected by the reader.

If you want to determine the connection bandwidth before receiving a sample, use this method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth">IWMReaderNetworkConfig::SetConnectionBandwidth</a>