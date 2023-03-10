---
UID: NF:wmsdkidl.IWMWriterNetworkSink.GetNetworkProtocol
title: IWMWriterNetworkSink::GetNetworkProtocol (wmsdkidl.h)
description: The GetNetworkProtocol method retrieves the network protocol that the network sink uses. Currently, HTTP is the only protocol the network sink supports.
helpviewer_keywords: ["GetNetworkProtocol","GetNetworkProtocol method [windows Media Format]","GetNetworkProtocol method [windows Media Format]","IWMWriterNetworkSink interface","IWMWriterNetworkSink interface [windows Media Format]","GetNetworkProtocol method","IWMWriterNetworkSink.GetNetworkProtocol","IWMWriterNetworkSink::GetNetworkProtocol","IWMWriterNetworkSinkGetNetworkProtocol","wmformat.iwmwriternetworksink_getnetworkprotocol","wmsdkidl/IWMWriterNetworkSink::GetNetworkProtocol"]
old-location: wmformat\iwmwriternetworksink_getnetworkprotocol.htm
tech.root: wmformat
ms.assetid: 5007b5be-9521-46f4-8e5c-85e70d48e99f
ms.date: 12/05/2018
ms.keywords: GetNetworkProtocol, GetNetworkProtocol method [windows Media Format], GetNetworkProtocol method [windows Media Format],IWMWriterNetworkSink interface, IWMWriterNetworkSink interface [windows Media Format],GetNetworkProtocol method, IWMWriterNetworkSink.GetNetworkProtocol, IWMWriterNetworkSink::GetNetworkProtocol, IWMWriterNetworkSinkGetNetworkProtocol, wmformat.iwmwriternetworksink_getnetworkprotocol, wmsdkidl/IWMWriterNetworkSink::GetNetworkProtocol
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
 - IWMWriterNetworkSink::GetNetworkProtocol
 - wmsdkidl/IWMWriterNetworkSink::GetNetworkProtocol
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
 - IWMWriterNetworkSink.GetNetworkProtocol
---

# IWMWriterNetworkSink::GetNetworkProtocol


## -description

The <b>GetNetworkProtocol</b> method retrieves the network protocol that the network sink uses. Currently, HTTP is the only protocol the network sink supports.

## -parameters

### -param pProtocol [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_net_protocol">WMT_NET_PROTOCOL</a> enumeration type.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, the values shown in the following table.

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
<i>pProtocol</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setnetworkprotocol">IWMWriterNetworkSink::SetNetworkProtocol</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_net_protocol">WMT_NET_PROTOCOL</a>