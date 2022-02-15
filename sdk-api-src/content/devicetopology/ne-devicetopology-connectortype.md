---
UID: NE:devicetopology.__MIDL___MIDL_itf_devicetopology_0000_0000_0013
title: ConnectorType (devicetopology.h)
description: The ConnectorType enumeration indicates the type of connection that a connector is part of.
helpviewer_keywords: ["ConnectorType","ConnectorType","ConnectorType enumeration [Core Audio]","Network","Physical_External","Physical_Internal","Software_Fixed","Software_IO","Unknown_Connector","coreaudio.connectortype","devicetopology/ConnectorType","devicetopology/Network","devicetopology/Physical_External","devicetopology/Physical_Internal","devicetopology/Software_Fixed","devicetopology/Software_IO","devicetopology/Unknown_Connector"]
old-location: coreaudio\connectortype.htm
tech.root: CoreAudio
ms.assetid: 7171a880-2a3e-45aa-803d-26bf5e9e0365
ms.date: 12/05/2018
ms.keywords: ConnectorType, ConnectorType , ConnectorType enumeration [Core Audio], Network, Physical_External, Physical_Internal, Software_Fixed, Software_IO, Unknown_Connector, coreaudio.connectortype, devicetopology/ConnectorType, devicetopology/Network, devicetopology/Physical_External, devicetopology/Physical_Internal, devicetopology/Software_Fixed, devicetopology/Software_IO, devicetopology/Unknown_Connector
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ConnectorType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_devicetopology_0000_0000_0013
 - devicetopology/__MIDL___MIDL_itf_devicetopology_0000_0000_0013
 - ConnectorType
 - devicetopology/ConnectorType
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
 - ConnectorType
---

# ConnectorType enumeration


## -description

The <b>ConnectorType</b> enumeration indicates the type of connection that a connector is part of.

## -enum-fields

### -field Unknown_Connector:0

The connector is part of a connection of unknown type.

### -field Physical_Internal

The connector is part of a physical connection to an auxiliary device that is installed inside the system chassis (for example, a connection to the analog output of an internal CD player, or to a built-in microphone or built-in speakers in a laptop computer).

### -field Physical_External

The connector is part of a physical connection to an external device. That is, the connector is a user-accessible jack that connects to a microphone, speakers, headphones, S/PDIF input or output device, or line input or output device.

### -field Software_IO

The connector is part of a software-configured I/O connection (typically a DMA channel) between system memory and an audio hardware device on an audio adapter.

### -field Software_Fixed

The connector is part of a permanent connection that is fixed and cannot be configured under software control. This type of connection is typically used to connect two audio hardware devices that reside on the same adapter.

### -field Network

The connector is part of a connection to a network.

## -remarks

The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-gettype">IConnector::GetType</a> method uses the constants defined in the <b>ConnectorType</b> enumeration.

For more information about connector types, see <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-constants">Core Audio Constants</a>



<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-gettype">IConnector::GetType</a>
