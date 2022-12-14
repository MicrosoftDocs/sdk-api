---
UID: NS:iphlpapi._INTERFACE_TIMESTAMP_CAPABILITIES
title: INTERFACE_TIMESTAMP_CAPABILITIES (iphlpapi.h)
description: Describes the exact timestamp capabilities that a network adapter supports.
helpviewer_keywords: ["*PINTERFACE_TIMESTAMP_CAPABILITIES","INTERFACE_TIMESTAMP_CAPABILITIES","INTERFACE_TIMESTAMP_CAPABILITIES structure [IP Helper]","PINTERFACE_TIMESTAMP_CAPABILITIES","PINTERFACE_TIMESTAMP_CAPABILITIES structure pointer [IP Helper]","iphlp.interface_timestamp_capabilities","iphlpapi/INTERFACE_TIMESTAMP_CAPABILITIES","iphlpapi/PINTERFACE_TIMESTAMP_CAPABILITIES"]
old-location: iphlp\interface_timestamp_capabilities.htm
tech.root: IpHlp
ms.assetid: 711D88F6-C57B-4BD1-A607-834CFE9D1BC1
ms.date: 12/16/2020
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11 (Build 10.0.22000.194)
req.target-min-winversvr: Windows Server 2022
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
req.typenames: INTERFACE_TIMESTAMP_CAPABILITIES, *PINTERFACE_TIMESTAMP_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERFACE_TIMESTAMP_CAPABILITIES
 - iphlpapi/_INTERFACE_TIMESTAMP_CAPABILITIES
 - PINTERFACE_TIMESTAMP_CAPABILITIES
 - iphlpapi/PINTERFACE_TIMESTAMP_CAPABILITIES
 - INTERFACE_TIMESTAMP_CAPABILITIES
 - iphlpapi/INTERFACE_TIMESTAMP_CAPABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iphlpapi.h
api_name:
 - INTERFACE_TIMESTAMP_CAPABILITIES
---

## -description

Describes the exact timestamp capabilities that a network adapter supports.

To retrieve the supported timestamp capabilities of a network adapter, call the [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) function. That function returns the supported timestamping capabilities in the form of an **INTERFACE_TIMESTAMP_CAPABILITIES** object.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -struct-fields

### -field HardwareClockFrequencyHz

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

Contains the frequency of the network adapter's hardware clock, rounded off to the nearest integer in Hertz units. Note this is the nominal frequency, and the actual frequency might not be the same as this. This data could be used to display the nominal clock frequency to end users for informational purposes. It's possible for *HardwareClockFrequencyHz* to contain the value 0.

### -field SupportsCrossTimestamp

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

A value of **TRUE** indicates that the network adapter driver is capable of generating a hardware cross timestamp. A cross timestamp refers to a set of network interface card (NIC) hardware timestamp and system timestamp(s) obtained very close to one another. A value of **FALSE** indicates that this capability doesn't exist.

### -field HardwareCapabilities

Type: **[INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_timestamp_capabilities)**

Describes the timestamping capabilities of the network interface card's (NIC's) hardware. Having both hardware and software timestamps enabled together isn't supported.

### -field SoftwareCapabilities

Type: **[INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_software_timestamp_capabilities)**

Describes the software timestamping capabilities of a network interface card's (NIC's) miniport driver. Having both hardware and software timestamps enabled together isn't supported.

## -see-also

[Packet timestamping](/windows/win32/iphlp/packet-timestamping)
