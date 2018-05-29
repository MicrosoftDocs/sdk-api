---
UID: NE:wmsdkidl.WMT_NET_PROTOCOL
title: WMT_NET_PROTOCOL
author: windows-sdk-content
description: The WMT_STREAM_SELECTION enumeration type defines the types of protocols that the network sink supports.
old-location: wmformat\wmt_net_protocol.htm
old-project: wmformat
ms.assetid: dc8b67a9-33fe-408b-b0b5-62a2b219b6b5
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WMT_NET_PROTOCOL, WMT_NET_PROTOCOL enumeration [windows Media Format], WMT_PROTOCOL_HTTP, wmformat.wmt_net_protocol, wmsdkidl/WMT_NET_PROTOCOL, wmsdkidl/WMT_PROTOCOL_HTTP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: WMT_NET_PROTOCOL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmsdkidl.h
api_name:
-	WMT_NET_PROTOCOL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMT_NET_PROTOCOL enumeration


## -description



The <b>WMT_STREAM_SELECTION</b> enumeration type defines the types of protocols that the network sink supports.




## -enum-fields




### -field WMT_PROTOCOL_HTTP

The network sink supports hypertext transfer protocol (HTTP).


## -remarks



This enumeration is used in two methods, <b>GetNetworkProtocol</b> and <b>SetNetworkProtocol</b>, from the <b>IWMWriterNetworkSink</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/5007b5be-9521-46f4-8e5c-85e70d48e99f">IWMWriterNetworkSink::GetNetworkProtocol</a>



<a href="https://msdn.microsoft.com/8ad6b2a4-b50b-45a0-8aa0-cabfc1e59bb7">IWMWriterNetworkSink::SetNetworkProtocol</a>
 

 

