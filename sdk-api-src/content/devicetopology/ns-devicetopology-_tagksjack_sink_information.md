---
UID: NS:devicetopology._tagKSJACK_SINK_INFORMATION
title: "_tagKSJACK_SINK_INFORMATION"
author: windows-sdk-content
description: The KSJACK_SINK_INFORMATION structure stores information about an audio jack sink.
old-location: coreaudio\ksjack_sink_information.htm
old-project: CoreAudio
ms.assetid: ee7211d8-a34f-40c9-9925-7bb40792bae9
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: KSJACK_SINK_INFORMATION, KSJACK_SINK_INFORMATION structure [Core Audio], PKSJACK_SINK_INFORMATION, PKSJACK_SINK_INFORMATION structure pointer [Core Audio], _tagKSJACK_SINK_INFORMATION, coreaudio.ksjack_sink_information, devicetopology/KSJACK_SINK_INFORMATION, devicetopology/PKSJACK_SINK_INFORMATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KSJACK_SINK_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Devicetopology.h
api_name:
-	KSJACK_SINK_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

