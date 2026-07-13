---
UID: NE:wmsdkidl.WMT_NET_PROTOCOL
title: WMT_NET_PROTOCOL (wmsdkidl.h)
description: The WMT_STREAM_SELECTION enumeration type defines the types of protocols that the network sink supports.
helpviewer_keywords: ["WMT_NET_PROTOCOL","WMT_NET_PROTOCOL enumeration [windows Media Format]","WMT_PROTOCOL_HTTP","wmformat.wmt_net_protocol","wmsdkidl/WMT_NET_PROTOCOL","wmsdkidl/WMT_PROTOCOL_HTTP"]
old-location: wmformat\wmt_net_protocol.htm
tech.root: wmformat
ms.assetid: dc8b67a9-33fe-408b-b0b5-62a2b219b6b5
ms.date: 4/26/2023
ms.keywords: WMT_NET_PROTOCOL, WMT_NET_PROTOCOL enumeration [windows Media Format], WMT_PROTOCOL_HTTP, wmformat.wmt_net_protocol, wmsdkidl/WMT_NET_PROTOCOL, wmsdkidl/WMT_PROTOCOL_HTTP
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMT_NET_PROTOCOL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_NET_PROTOCOL
 - wmsdkidl/WMT_NET_PROTOCOL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_NET_PROTOCOL
---

# WMT_NET_PROTOCOL enumeration


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_STREAM_SELECTION</b> enumeration type defines the types of protocols that the network sink supports.

## -enum-fields

### -field WMT_PROTOCOL_HTTP:0

The network sink supports hypertext transfer protocol (HTTP).

## -remarks

This enumeration is used in two methods, <b>GetNetworkProtocol</b> and <b>SetNetworkProtocol</b>, from the <b>IWMWriterNetworkSink</b> interface.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-getnetworkprotocol">IWMWriterNetworkSink::GetNetworkProtocol</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setnetworkprotocol">IWMWriterNetworkSink::SetNetworkProtocol</a>
