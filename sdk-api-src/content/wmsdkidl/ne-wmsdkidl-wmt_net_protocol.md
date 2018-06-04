---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

