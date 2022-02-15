---
UID: NS:iphlpapi._INTERFACE_HARDWARE_CROSSTIMESTAMP
title: INTERFACE_HARDWARE_CROSSTIMESTAMP (iphlpapi.h)
description: Describes a cross timestamp retrieved from a network adapter.
helpviewer_keywords: ["*PINTERFACE_HARDWARE_CROSSTIMESTAMP","INTERFACE_HARDWARE_CROSSTIMESTAMP","INTERFACE_HARDWARE_CROSSTIMESTAMP structure [IP Helper]","PINTERFACE_HARDWARE_CROSSTIMESTAMP","PINTERFACE_HARDWARE_CROSSTIMESTAMP structure pointer [IP Helper]","iphlp.interface_hardware_crosstimestamp","iphlpapi/INTERFACE_HARDWARE_CROSSTIMESTAMP","iphlpapi/PINTERFACE_HARDWARE_CROSSTIMESTAMP"]
old-location: iphlp\interface_hardware_crosstimestamp.htm
tech.root: IpHlp
ms.assetid: DAEA7430-85C1-4FF5-8F85-C58EDF27BF3D
ms.date: 12/03/2020
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
req.typenames: INTERFACE_HARDWARE_CROSSTIMESTAMP, *PINTERFACE_HARDWARE_CROSSTIMESTAMP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERFACE_HARDWARE_CROSSTIMESTAMP
 - iphlpapi/_INTERFACE_HARDWARE_CROSSTIMESTAMP
 - PINTERFACE_HARDWARE_CROSSTIMESTAMP
 - iphlpapi/PINTERFACE_HARDWARE_CROSSTIMESTAMP
 - INTERFACE_HARDWARE_CROSSTIMESTAMP
 - iphlpapi/INTERFACE_HARDWARE_CROSSTIMESTAMP
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
 - INTERFACE_HARDWARE_CROSSTIMESTAMP
---

## -description

Describes a cross timestamp retrieved from a network adapter. A cross timestamp refers to a set of network interface card (NIC) hardware timestamp and system timestamp(s) obtained very close to one another.

To retrieve a cross timestamp, call the [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) function. That function returns the timestamp from the network adapter in the form of an **INTERFACE_HARDWARE_CROSSTIMESTAMP** object.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -struct-fields

### -field SystemTimestamp1

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

The network adapter driver fills this with a system timestamp whose value corresponds to a value returned by [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).

*SystemTimestamp1* is obtained before *HardwareClockTimestamp*; while *SystemTimestamp2* is taken after *HardwareClockTimestamp*. The timestamp values are obtained as closely as possible to each other.

### -field HardwareClockTimestamp

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

The network adapter driver fills this with a value obtained from its network interface card (NIC) hardware clock.

### -field SystemTimestamp2

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

The network adapter driver fills this with a system timestamp whose value corresponds to a value returned by [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).

*SystemTimestamp1* is obtained before *HardwareClockTimestamp*; while *SystemTimestamp2* is taken after *HardwareClockTimestamp*. The timestamp values are obtained as closely as possible to each other.

## -see-also

[Packet timestamping](/windows/win32/iphlp/packet-timestamping)
