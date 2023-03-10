---
UID: NF:iphlpapi.CaptureInterfaceHardwareCrossTimestamp
title: CaptureInterfaceHardwareCrossTimestamp function (iphlpapi.h)
description: Retrieves cross timestamp info for a network adapter.
helpviewer_keywords: ["CaptureInterfaceHardwareCrossTimestamp","CaptureInterfaceHardwareCrossTimestamp function [IP Helper]","iphlp.captureinterfacehardwarecrosstimestamp","iphlpapi/CaptureInterfaceHardwareCrossTimestamp"]
old-location: iphlp\captureinterfacehardwarecrosstimestamp.htm
tech.root: IpHlp
ms.assetid: FB3C27CD-7D56-40F3-9DF9-A1115772D1C6
ms.date: 12/02/2020
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CaptureInterfaceHardwareCrossTimestamp
 - iphlpapi/CaptureInterfaceHardwareCrossTimestamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CaptureInterfaceHardwareCrossTimestamp
---

## -description

Retrieves cross timestamp info for a network adapter.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

> [!IMPORTANT]
> On Windows 10, version 2004 (10.0; Build 19041) and earlier, this function is reserved for system use, and you should not call it from your code. On later versions, this function *is* supported.

## -parameters

### -param InterfaceLuid

Type: \_In\_ **CONST [NET_LUID](/windows/win32/api/ifdef/ns-ifdef-net_luid_lh)\***

The network locally unique identifier (LUID) of the network adapter from which a cross timestamp is to be retrieved.

### -param CrossTimestamp

Type: \_Inout\_ **[PINTERFACE_HARDWARE_CROSSTIMESTAMP](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp)**

The timestamp is returned by the network adapter in the form of an [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) object.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

A **DWORD** return code indicating success or failure.

## -see-also

[Packet timestamping](/windows/win32/iphlp/packet-timestamping)
