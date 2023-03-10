---
UID: NF:iphlpapi.RegisterInterfaceTimestampConfigChange
title: RegisterInterfaceTimestampConfigChange
description: Registers a user-implemented callback function, which the system calls to notify you of a timestamp capability change.
helpviewer_keywords: ["RegisterInterfaceTimestampConfigChange","RegisterInterfaceTimestampConfigChange function [IP Helper]","iphlp.registerinterfacetimestampconfigchange","iphlpapi/RegisterInterfaceTimestampConfigChange"]
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
 - RegisterInterfaceTimestampConfigChange
 - iphlpapi/RegisterInterfaceTimestampConfigChange
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
 - RegisterInterfaceTimestampConfigChange
---

## -description

Registers a user-implemented callback function, which the system calls to notify you of a timestamp capability change. You can cancel the registration by calling [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange).

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -parameters

### -param Callback

Type: \_In\_ **[PINTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK](/windows/win32/api/iphlpapi/nc-iphlpapi-interface_timestamp_config_change_callback)**

Your callback function, to be invoked when a timestamp capability change happens.

### -param CallerContext

Type: \_In_opt\_ **PVOID**

An optional caller-allocated context.

### -param NotificationHandle

Type: \_Out\_ **HIFTIMESTAMPCHANGE**

A handle, returned by the function, that identifies the registration.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

A **DWORD** return code indicating success or failure.

## -remarks

## -see-also

* [Packet timestamping](/windows/win32/iphlp/packet-timestamping)
* [UnregisterInterfaceTimestampConfigChange](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange)
