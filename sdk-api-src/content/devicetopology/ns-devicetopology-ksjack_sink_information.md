---
UID: NS:devicetopology._tagKSJACK_SINK_INFORMATION
title: KSJACK_SINK_INFORMATION (devicetopology.h)
description: The KSJACK_SINK_INFORMATION structure stores information about an audio jack sink.
helpviewer_keywords: ["KSJACK_SINK_INFORMATION","KSJACK_SINK_INFORMATION structure [Core Audio]","PKSJACK_SINK_INFORMATION","PKSJACK_SINK_INFORMATION structure pointer [Core Audio]","coreaudio.ksjack_sink_information","devicetopology/KSJACK_SINK_INFORMATION","devicetopology/PKSJACK_SINK_INFORMATION"]
old-location: coreaudio\ksjack_sink_information.htm
tech.root: CoreAudio
ms.assetid: ee7211d8-a34f-40c9-9925-7bb40792bae9
ms.date: 12/05/2018
ms.keywords: KSJACK_SINK_INFORMATION, KSJACK_SINK_INFORMATION structure [Core Audio], PKSJACK_SINK_INFORMATION, PKSJACK_SINK_INFORMATION structure pointer [Core Audio], coreaudio.ksjack_sink_information, devicetopology/KSJACK_SINK_INFORMATION, devicetopology/PKSJACK_SINK_INFORMATION
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KSJACK_SINK_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagKSJACK_SINK_INFORMATION
 - devicetopology/_tagKSJACK_SINK_INFORMATION
 - KSJACK_SINK_INFORMATION
 - devicetopology/KSJACK_SINK_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - KSJACK_SINK_INFORMATION
---

# KSJACK_SINK_INFORMATION structure


## -description

The <b>KSJACK_SINK_INFORMATION</b> structure stores information about an audio jack sink.

## -struct-fields

### -field ConnType

Specifies the type of connection. The connection type values are defined in the  <a href="/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype">KSJACK_SINK_CONNECTIONTYPE</a> enumeration.

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

Specifies the video port identifier in a <a href="/windows/desktop/api/devicetopology/ns-devicetopology-luid">LUID</a> structure.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation">IKsJackSinkInformation::GetJackSinkInformation</a>