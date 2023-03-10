---
UID: NF:iphlpapi.UnregisterInterfaceTimestampConfigChange
title: UnregisterInterfaceTimestampConfigChange
description: Cancels notifications about timestamp capability changes by unregistering the callback function you registered in a call to [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange).
helpviewer_keywords: ["UnregisterInterfaceTimestampConfigChange","UnregisterInterfaceTimestampConfigChange function [IP Helper]","iphlp.unregisterinterfacetimestampconfigchange","iphlpapi/UnregisterInterfaceTimestampConfigChange"]
tech.root: IpHlp
ms.date: 12/18/2020
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
 - UnregisterInterfaceTimestampConfigChange
 - iphlpapi/UnregisterInterfaceTimestampConfigChange
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
 - UnregisterInterfaceTimestampConfigChange
---

## -description

Cancels notifications about timestamp capability changes by unregistering the callback function you registered in a call to [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange).

To avoid deadlock, you shouldn't call **UnregisterInterfaceTimestampConfigChange** in the context of the thread that's executing a callback that was specified to **RegisterInterfaceTimestampConfigChange**. This is because **UnregisterInterfaceTimestampConfigChange** waits for outstanding notification callbacks to complete before it returns. Consequently, **UnregisterInterfaceTimestampConfigChange** mustn't be called in a way that prevents an outstanding notification callback from completing. No further callbacks will take place after **UnregisterInterfaceTimestampConfigChange** returns.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -parameters

### -param NotificationHandle

Type: \_In\_ **HIFTIMESTAMPCHANGE**

The handle that was returned by [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange). This identifies the registration to be canceled.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

A **DWORD** return code indicating success or failure.

## -remarks

## -see-also

* [Packet timestamping](/windows/win32/iphlp/packet-timestamping)
* [RegisterInterfaceTimestampConfigChange](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
