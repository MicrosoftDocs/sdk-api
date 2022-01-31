---
UID: NE:fwpmtypes.FWPM_ENGINE_OPTION_
title: FWPM_ENGINE_OPTION (fwpmtypes.h)
description: Configurable options for the filter engine.
helpviewer_keywords: ["FWPM_ENGINE_COLLECT_NET_EVENTS","FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS","FWPM_ENGINE_NAME_CACHE","FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS","FWPM_ENGINE_OPTION","FWPM_ENGINE_OPTION enumeration [Filtering]","FWPM_ENGINE_OPTION_MAX","FWPM_ENGINE_PACKET_QUEUING","FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC","fwp.fwpm_engine_option","fwpmtypes/FWPM_ENGINE_COLLECT_NET_EVENTS","fwpmtypes/FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS","fwpmtypes/FWPM_ENGINE_NAME_CACHE","fwpmtypes/FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS","fwpmtypes/FWPM_ENGINE_OPTION","fwpmtypes/FWPM_ENGINE_OPTION_MAX","fwpmtypes/FWPM_ENGINE_PACKET_QUEUING","fwpmtypes/FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC"]
old-location: fwp\fwpm_engine_option.htm
tech.root: fwp
ms.assetid: e70986af-0c38-4fe6-a59f-3c45ce98bcc0
ms.date: 12/05/2018
ms.keywords: FWPM_ENGINE_COLLECT_NET_EVENTS, FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS, FWPM_ENGINE_NAME_CACHE, FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS, FWPM_ENGINE_OPTION, FWPM_ENGINE_OPTION enumeration [Filtering], FWPM_ENGINE_OPTION_MAX, FWPM_ENGINE_PACKET_QUEUING, FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC, fwp.fwpm_engine_option, fwpmtypes/FWPM_ENGINE_COLLECT_NET_EVENTS, fwpmtypes/FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS, fwpmtypes/FWPM_ENGINE_NAME_CACHE, fwpmtypes/FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS, fwpmtypes/FWPM_ENGINE_OPTION, fwpmtypes/FWPM_ENGINE_OPTION_MAX, fwpmtypes/FWPM_ENGINE_PACKET_QUEUING, fwpmtypes/FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_ENGINE_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_ENGINE_OPTION_
 - fwpmtypes/FWPM_ENGINE_OPTION_
 - FWPM_ENGINE_OPTION
 - fwpmtypes/FWPM_ENGINE_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_ENGINE_OPTION
---

# FWPM_ENGINE_OPTION enumeration


## -description

The <b>FWPM_ENGINE_OPTION</b> enumerated type specifies configurable options for the filter engine.

## -enum-fields

### -field FWPM_ENGINE_COLLECT_NET_EVENTS:0

The filter engine will collect WFP network events.

### -field FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS

The filter engine will collect WFP network events that match any supplied key words.

### -field FWPM_ENGINE_NAME_CACHE

Reserved for internal use.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS

Enables the connection monitoring feature and starts logging creation and deletion events (and notifying any subscribers).


If the ETW operational log is already enabled, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmenginegetoption0">FwpmEngineGetOption0</a> will return showing the option as enabled. <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmenginesetoption0">FwpmEngineSetOption0</a> can be used set the value (but fails with FWP_E_STILL_ON ERROR when attempting to disable it).


<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_ENGINE_PACKET_QUEUING

Enables inbound or forward packet queuing independently.   When enabled, the system is able to evenly distribute CPU load to multiple CPUs for site-to-site IPsec tunnel scenarios.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC

Transactions lasting longer than this time (in milliseconds) will trigger a
   watchdog event.


<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_ENGINE_OPTION_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/logging">Logging</a>



<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
