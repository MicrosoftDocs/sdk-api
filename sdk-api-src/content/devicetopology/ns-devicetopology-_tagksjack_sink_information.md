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

# _tagKSJACK_SINK_INFORMATION structure


## -description


The <b>KSJACK_SINK_INFORMATION</b> structure stores information about an audio jack sink.


## -struct-fields




### -field ConnType

Specifies the type of connection. The connection type values are defined in the  <a href="https://msdn.microsoft.com/a1a9b0cf-b1bf-49df-a976-62f44fcf70ae">KSJACK_SINK_CONNECTIONTYPE</a> enumeration.


### -field ManufacturerId

Specifies the sink manufacturer identifier.


### -field ProductId

Specifies the sink product identifier.


### -field AudioLatency

Specifies the latency of the audio sink.


### -field HDCPCapable

Specifies whether the sink supports High-bandwidth Digital Content Protection (HDCP).


### -field AICapable

 Specifies whether the sink supports ACP Packet, ISRC1, or ISRC2.


### -field SinkDescriptionLength

Specifies the length of the string in the <b>SinkDescription</b> member.


### -field SinkDescription

String containing the monitor sink name. The maximum length is defined by the constant <b>MAX_SINK_DESCRIPTION_NAME_LENGTH</b> (32 wide characters).


### -field PortId

Specifies the video port identifier in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/ca4165ce-433a-4a8f-9853-bbe812de90ca">IKsJackSinkInformation::GetJackSinkInformation</a>
 

 

