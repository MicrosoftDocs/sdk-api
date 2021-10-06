---
UID: NC:iphlpapi.INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK
title: INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK (iphlpapi.h)
description: A callback function that you implement in your app in order to be notified of changes to the timestamp capabilities of a network adapter.
helpviewer_keywords: ["INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK","INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK callback","INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK callback function [IP Helper]","iphlp.interface_timestamp_config_change_callback","iphlpapi/INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK"]
old-location: iphlp\interface_timestamp_config_change_callback.htm
tech.root: IpHlp
ms.assetid: 8B59F5F5-BBD2-4338-9FC6-40FA81DBC59A
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK
 - iphlpapi/INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - iphlpapi.h
api_name:
 - INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK
---

## -description

A callback function that you implement in your app in order to be notified of changes to the timestamp capabilities of a network adapter. Pass a pointer to your implementation when you call [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange).

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -parameters

### -param CallerContext

Type: \_In\_ **PVOID**

The caller-allocated context that you passed to [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange), or **NULL** if you didn't pass a context.

## -see-also

[Packet timestamping](/windows/win32/iphlp/packet-timestamping)
