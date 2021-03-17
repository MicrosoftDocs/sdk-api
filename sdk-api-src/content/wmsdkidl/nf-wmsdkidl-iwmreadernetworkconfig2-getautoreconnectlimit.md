---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetAutoReconnectLimit
title: IWMReaderNetworkConfig2::GetAutoReconnectLimit (wmsdkidl.h)
description: The GetAutoReconnectLimit method retrieves the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection.
helpviewer_keywords: ["GetAutoReconnectLimit","GetAutoReconnectLimit method [windows Media Format]","GetAutoReconnectLimit method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetAutoReconnectLimit method","IWMReaderNetworkConfig2.GetAutoReconnectLimit","IWMReaderNetworkConfig2::GetAutoReconnectLimit","IWMReaderNetworkConfig2GetAutoReconnectLimit","wmformat.iwmreadernetworkconfig2_getautoreconnectlimit","wmsdkidl/IWMReaderNetworkConfig2::GetAutoReconnectLimit"]
old-location: wmformat\iwmreadernetworkconfig2_getautoreconnectlimit.htm
tech.root: wmformat
ms.assetid: 8d0b794c-b3bf-4ec5-ac68-9666e73f7a6e
ms.date: 12/05/2018
ms.keywords: GetAutoReconnectLimit, GetAutoReconnectLimit method [windows Media Format], GetAutoReconnectLimit method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetAutoReconnectLimit method, IWMReaderNetworkConfig2.GetAutoReconnectLimit, IWMReaderNetworkConfig2::GetAutoReconnectLimit, IWMReaderNetworkConfig2GetAutoReconnectLimit, wmformat.iwmreadernetworkconfig2_getautoreconnectlimit, wmsdkidl/IWMReaderNetworkConfig2::GetAutoReconnectLimit
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
 - IWMReaderNetworkConfig2::GetAutoReconnectLimit
 - wmsdkidl/IWMReaderNetworkConfig2::GetAutoReconnectLimit
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
 - IWMReaderNetworkConfig2.GetAutoReconnectLimit
---

# IWMReaderNetworkConfig2::GetAutoReconnectLimit


## -description

The <b>GetAutoReconnectLimit</b> method retrieves the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection. This feature, called Fast Reconnect, applies only to content being streamed from a server running Windows Media Services.

## -parameters

### -param pdwAutoReconnectLimit [out]

Pointer to a <b>DWORD</b> containing the automatic reconnection limit.

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



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setautoreconnectlimit">IWMReaderNetworkConfig2::SetAutoReconnectLimit</a>