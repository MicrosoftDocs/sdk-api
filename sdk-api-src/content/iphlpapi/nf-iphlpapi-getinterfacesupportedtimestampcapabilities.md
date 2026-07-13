---
UID: NF:iphlpapi.GetInterfaceSupportedTimestampCapabilities
title: GetInterfaceSupportedTimestampCapabilities
description: Retrieves the supported timestamp capabilities of a network adapter.
helpviewer_keywords: ["GetInterfaceSupportedTimestampCapabilities","GetInterfaceSupportedTimestampCapabilities function [IP Helper]","iphlp.getinterfacesupportedtimestampcapabilities","iphlpapi/GetInterfaceSupportedTimestampCapabilities"]
tech.root: IpHlp
ms.date: 01/06/2021
req.construct-type: function
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - GetInterfaceSupportedTimestampCapabilities
 - iphlpapi/GetInterfaceSupportedTimestampCapabilities
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
 - GetInterfaceSupportedTimestampCapabilities
---

## -description

Retrieves the supported timestamp capabilities of a network adapter.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -parameters

### -param InterfaceLuid

Type: \_In\_ **CONST [NET_LUID](/windows/win32/api/ifdef/ns-ifdef-net_luid_lh)\***

The network locally unique identifier (LUID) of the network adapter for which supported timestamp capabilities are to be retrieved.

### -param TimestampCapabilites

Type: \_Out\_ **[PINTERFACE_TIMESTAMP_CAPABILITIES](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities)**

If the function succeeds, then *TimestampCapabilites* returns a structure that describes the supported timestamp capabilities.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds, then it returns **NO_ERROR**. If the network card corresponding to *InterfaceLuid* isn't timestamp-aware, then the function returns **ERROR_NOT_SUPPORTED**.

## -remarks

## -see-also

* [Packet timestamping](/windows/win32/iphlp/packet-timestamping)
