---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetMaxNetPacketSize
title: IWMReaderNetworkConfig2::GetMaxNetPacketSize (wmsdkidl.h)
description: The GetMaxNetPacketSize method retrieves the maximum size of packets being streamed over a network.
helpviewer_keywords: ["GetMaxNetPacketSize","GetMaxNetPacketSize method [windows Media Format]","GetMaxNetPacketSize method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetMaxNetPacketSize method","IWMReaderNetworkConfig2.GetMaxNetPacketSize","IWMReaderNetworkConfig2::GetMaxNetPacketSize","IWMReaderNetworkConfig2GetMaxNetPacketSize","wmformat.iwmreadernetworkconfig2_getmaxnetpacketsize","wmsdkidl/IWMReaderNetworkConfig2::GetMaxNetPacketSize"]
old-location: wmformat\iwmreadernetworkconfig2_getmaxnetpacketsize.htm
tech.root: wmformat
ms.assetid: 0249822c-4772-4317-aec2-e466fbd70bad
ms.date: 12/05/2018
ms.keywords: GetMaxNetPacketSize, GetMaxNetPacketSize method [windows Media Format], GetMaxNetPacketSize method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetMaxNetPacketSize method, IWMReaderNetworkConfig2.GetMaxNetPacketSize, IWMReaderNetworkConfig2::GetMaxNetPacketSize, IWMReaderNetworkConfig2GetMaxNetPacketSize, wmformat.iwmreadernetworkconfig2_getmaxnetpacketsize, wmsdkidl/IWMReaderNetworkConfig2::GetMaxNetPacketSize
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderNetworkConfig2::GetMaxNetPacketSize
 - wmsdkidl/IWMReaderNetworkConfig2::GetMaxNetPacketSize
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
 - IWMReaderNetworkConfig2.GetMaxNetPacketSize
---

# IWMReaderNetworkConfig2::GetMaxNetPacketSize


## -description

The <b>GetMaxNetPacketSize</b> method retrieves the maximum size of packets being streamed over a network.

## -parameters

### -param pdwMaxNetPacketSize [out]

Pointer to a <b>DWORD</b> containing the maximum net packet size, in bytes.

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
NULL pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>