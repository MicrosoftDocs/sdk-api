---
UID: NS:nldef._NL_NETWORK_CONNECTIVITY_HINT
title: NL_NETWORK_CONNECTIVITY_HINT
author: windows-sdk-content
description: Describes a level of network connectivity, the usage charge for a network connection, and other members reflecting cost factors.
tech.root: IpHlp
ms.author: windowssdkdev
ms.date: 10/21/2019
ms.keywords: _NL_NETWORK_CONNECTIVITY_HINT, NL_NETWORK_CONNECTIVITY_HINT
req.header: nldef.h
req.include-header: iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
req.typenames: NL_NETWORK_CONNECTIVITY_HINT
req.redist: 
f1_keywords:
 - _NL_NETWORK_CONNECTIVITY_HINT
 - nldef/_NL_NETWORK_CONNECTIVITY_HINT
 - NL_NETWORK_CONNECTIVITY_HINT
 - nldef/NL_NETWORK_CONNECTIVITY_HINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nldef.h
api_name:
 - _NL_NETWORK_CONNECTIVITY_HINT
 - NL_NETWORK_CONNECTIVITY_HINT
---

## -description

Describes a level of network connectivity, the usage charge for a network connection, and other members reflecting cost factors.

The last four members of **NL_NETWORK_CONNECTIVITY_HINT** collectively work together to allow you to resolve the cost of using a connection. See the guidelines in 
[How to manage metered network cost constraints](/previous-versions/windows/apps/jj835821(v=win.10)).

## -struct-fields

### -field ConnectivityLevel

Type: **[NL_NETWORK_CONNECTIVITY_LEVEL_HINT](./ne-nldef-nl_network_connectivity_level_hint.md)**

The level of network connectivity.

### -field ConnectivityCost

Type: **[NL_NETWORK_CONNECTIVITY_COST_HINT](./ne-nldef-nl_network_connectivity_cost_hint.md)**

The usage charge for the network connection.

### -field ApproachingDataLimit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` if the connection is approaching its data limit, otherwise `FALSE`.

### -field OverDataLimit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` if the connection has exceeded its data limit, otherwise `FALSE`.

### -field Roaming

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` if the connection is roaming, otherwise `FALSE`.

## -remarks

## -see-also

[How to manage metered network cost constraints](/previous-versions/windows/apps/jj835821(v=win.10))