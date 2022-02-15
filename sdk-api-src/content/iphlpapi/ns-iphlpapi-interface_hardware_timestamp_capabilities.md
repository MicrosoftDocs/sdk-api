---
UID: NS:iphlpapi._INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
title: INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
description: Describes the timestamping capabilities of a network interface card's (NIC's) hardware.
helpviewer_keywords: ["*PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES","INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES","INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES structure [IP Helper]","PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES","PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES structure pointer [IP Helper]","iphlp.INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES","iphlpapi/INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES","iphlpapi/PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES"]
tech.root: IpHlp
ms.date: 12/16/2020
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES, *PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
req.redist: 
f1_keywords:
 - _INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - iphlpapi/_INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - iphlpapi/PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - iphlpapi/INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
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
 - _INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - PINTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
 - INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES
---

## -description

Describes the timestamping capabilities of a network interface card's (NIC's) hardware.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -struct-fields

### -field PtpV2OverUdpIPv4EventMessageReceive

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that, during packet reception, the NIC can recognize in hardware a PTP version 2 event message contained in an IPv4 UDP packet, and can generate a timestamp in hardware corresponding to when such a packet was received. A value of **FALSE** indicates that the hardware is not capable of this.

### -field PtpV2OverUdpIPv4AllMessageReceive

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that, during packet reception, the NIC can recognize in hardware any PTP version 2 message (not just PTP event messages) contained in an IPv4 UDP packet, and can generate a timestamp in hardware corresponding to when such a packet was received. A value of **FALSE** indicates that the hardware is not capable of this.

### -field PtpV2OverUdpIPv4EventMessageTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that, during packet transmission, the NIC can recognize in hardware a PTP version 2 event message contained in an IPv4 UDP packet, and can generate a timestamp in hardware corresponding to when such a packet was transmitted. A value of **FALSE** indicates that the hardware is not capable of this.

### -field PtpV2OverUdpIPv4AllMessageTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that, during packet transmission, the NIC can recognize in hardware any PTP version 2 message (not just PTP event messages) contained in an IPv4 UDP packet, and can generate a timestamp in hardware corresponding to when such a packet was transmitted. A value of **FALSE** indicates that the hardware is not capable of this.

### -field PtpV2OverUdpIPv6EventMessageReceive

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

The same as *PtpV2OverUdpIPv4EventMsgReceiveHw*, except that it applies to IPv6.

### -field PtpV2OverUdpIPv6AllMessageReceive

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

The same as *PtpV2OverUdpIPv4AllMsgReceiveHw*, except that it applies to IPv6.

### -field PtpV2OverUdpIPv6EventMessageTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

The same as *PtpV2OverUdpIPv4EventMsgTransmitHw*, except that it applies to IPv6.

### -field PtpV2OverUdpIPv6AllMessageTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

The same as *PtpV2OverUdpIPv4AllMsgTransmitHw*, except that it applies to IPv6.

### -field AllReceive

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that the NIC can generate a hardware timestamp for all received packets (that is, not just PTP). A value of **FALSE** indicates that the hardware is not capable of this.

### -field AllTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that the NIC can generate a hardware timestamp for all transmitted packets (that is, not just PTP). A value of **FALSE** indicates that the hardware is not capable of this.

### -field TaggedTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

**TRUE** indicates that the NIC can generate a hardware timestamp for any specific transmitted packet when indicated to do so by the application. A value of **FALSE** indicates that the hardware is not capable of this.
See [**TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) (and **TIMESTAMPING_FLAG_TX**) to determine how to request a timestamp when sending UDP packets through [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2).

## -remarks

All of the **INTERFACE_HARDWARE_TIMESTAMP_CAPABILITIES** structure's members represent hardware timestamp capabilities. The hardware timestamps are generated using the NIC's hardware clock.

Having both hardware and software timestamps enabled together isn't supported.

## -see-also

* [Packet timestamping](/windows/win32/iphlp/packet-timestamping)
