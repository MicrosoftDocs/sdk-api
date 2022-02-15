---
UID: NE:nldef._NL_NETWORK_CONNECTIVITY_COST_HINT
title: NL_NETWORK_CONNECTIVITY_COST_HINT
author: windows-sdk-content
description: Defines constants that specify hints about the usage charge for a network connection.
tech.root: IpHlp
ms.author: windowssdkdev
ms.date: 10/21/2019
ms.keywords: _NL_NETWORK_CONNECTIVITY_COST_HINT, NL_NETWORK_CONNECTIVITY_COST_HINT
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
req.typenames: NL_NETWORK_CONNECTIVITY_COST_HINT
req.redist: 
f1_keywords:
 - _NL_NETWORK_CONNECTIVITY_COST_HINT
 - nldef/_NL_NETWORK_CONNECTIVITY_COST_HINT
 - NL_NETWORK_CONNECTIVITY_COST_HINT
 - nldef/NL_NETWORK_CONNECTIVITY_COST_HINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - nldef.h
api_name:
 - _NL_NETWORK_CONNECTIVITY_COST_HINT
 - NL_NETWORK_CONNECTIVITY_COST_HINT
---

## -description

Defines constants that specify hints about the usage charge for a network connection.

## -enum-fields

### -field NetworkConnectivityCostHintUnknown:0

Specifies a hint that cost information is not available.

### -field NetworkConnectivityCostHintUnrestricted

Specifies a hint that the connection is unlimited, and has unrestricted usage charges and capacity constraints.

### -field NetworkConnectivityCostHintFixed

Specifies a hint that the use of the connection is unrestricted up to a specific limit.

### -field NetworkConnectivityCostHintVariable

Specifies a hint that the connection is charged on a per-byte basis.

## -remarks

## -see-also

