---
UID: NS:psapi._PSAPI_WS_WATCH_INFORMATION
title: PSAPI_WS_WATCH_INFORMATION (psapi.h)
description: Contains information about a page added to a process working set.
helpviewer_keywords: ["*PPSAPI_WS_WATCH_INFORMATION","PPSAPI_WS_WATCH_INFORMATION","PPSAPI_WS_WATCH_INFORMATION structure pointer [PSAPI]","PSAPI_WS_WATCH_INFORMATION","PSAPI_WS_WATCH_INFORMATION structure [PSAPI]","_win32_psapi_ws_watch_information_str","base.psapi_ws_watch_information_str","psapi.psapi_ws_watch_information_str","psapi/PPSAPI_WS_WATCH_INFORMATION","psapi/PSAPI_WS_WATCH_INFORMATION"]
old-location: psapi\psapi_ws_watch_information_str.htm
tech.root: psapi
ms.assetid: 61083366-2a55-431c-807a-3eb85ba0b347
ms.date: 12/05/2018
ms.keywords: '*PPSAPI_WS_WATCH_INFORMATION, PPSAPI_WS_WATCH_INFORMATION, PPSAPI_WS_WATCH_INFORMATION structure pointer [PSAPI], PSAPI_WS_WATCH_INFORMATION, PSAPI_WS_WATCH_INFORMATION structure [PSAPI], _win32_psapi_ws_watch_information_str, base.psapi_ws_watch_information_str, psapi.psapi_ws_watch_information_str, psapi/PPSAPI_WS_WATCH_INFORMATION, psapi/PSAPI_WS_WATCH_INFORMATION'
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PSAPI_WS_WATCH_INFORMATION, *PPSAPI_WS_WATCH_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSAPI_WS_WATCH_INFORMATION
 - psapi/_PSAPI_WS_WATCH_INFORMATION
 - PPSAPI_WS_WATCH_INFORMATION
 - psapi/PPSAPI_WS_WATCH_INFORMATION
 - PSAPI_WS_WATCH_INFORMATION
 - psapi/PSAPI_WS_WATCH_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - PSAPI_WS_WATCH_INFORMATION
---

# PSAPI_WS_WATCH_INFORMATION structure


## -description

Contains information about a page added to a process working set.

## -struct-fields

### -field FaultingPc

A pointer to the instruction that caused the page fault.

### -field FaultingVa

A pointer to the page that was added to the working set.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-getwschanges">GetWsChanges</a>