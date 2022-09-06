---
UID: NE:nldef._NL_NETWORK_CONNECTIVITY_LEVEL_HINT
title: NL_NETWORK_CONNECTIVITY_LEVEL_HINT
author: windows-sdk-content
description: Defines constants that specify hints about a level of network connectivity.
tech.root: IpHlp
ms.author: windowssdkdev
ms.date: 10/21/2019
ms.keywords: _NL_NETWORK_CONNECTIVITY_LEVEL_HINT, NL_NETWORK_CONNECTIVITY_LEVEL_HINT
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
req.typenames: NL_NETWORK_CONNECTIVITY_LEVEL_HINT
req.redist: 
f1_keywords:
 - _NL_NETWORK_CONNECTIVITY_LEVEL_HINT
 - nldef/_NL_NETWORK_CONNECTIVITY_LEVEL_HINT
 - NL_NETWORK_CONNECTIVITY_LEVEL_HINT
 - nldef/NL_NETWORK_CONNECTIVITY_LEVEL_HINT
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
 - _NL_NETWORK_CONNECTIVITY_LEVEL_HINT
 - NL_NETWORK_CONNECTIVITY_LEVEL_HINT
---

## -description

Defines constants that specify hints about a level of network connectivity.

## -enum-fields

### -field NetworkConnectivityLevelHintUnknown:0

Specifies a hint for an unknown level of connectivity. There is a short window of time during Windows (or application container) boot when this value might be returned.

### -field NetworkConnectivityLevelHintNone

Specifies a hint for no connectivity.

### -field NetworkConnectivityLevelHintLocalAccess

Specifies a hint for local network access only.

### -field NetworkConnectivityLevelHintInternetAccess

Specifies a hint for local and internet access.

### -field NetworkConnectivityLevelHintConstrainedInternetAccess

Specifies a hint for limited internet access.

This value indicates captive portal connectivity, where local access to a web portal is provided, but access to the internet requires that specific credentials are provided via the portal. This level of connectivity is generally encountered when using connections hosted in public locations (for example, coffee shops and book stores).

This doesn't guarantee detection of a captive portal. You should be aware that when Windows reports the connectivity level hint as **NetworkConnectivityLevelHintLocalAccess**, your application's network requests might be redirected, and thus receive a different response than expected. Other protocols might also be impacted; for example, HTTPS might be redirected, and fail authentication.

### -field NetworkConnectivityLevelHintHidden

Specifies a hint for a network interface that's hidden from normal connectivity (and is not, by default, accessible to applications). This could be because no packets are allowed at all over that network (for example, the adapter flags itself **NCF_HIDDEN**), or (by default) routes are ignored on that interface (for example, a cellular network is hidden when WiFi is connected).

## -remarks

## -see-also

