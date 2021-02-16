---
UID: NS:psapi._PSAPI_WS_WATCH_INFORMATION_EX
title: PSAPI_WS_WATCH_INFORMATION_EX (psapi.h)
description: Contains extended information about a page added to a process working set.
helpviewer_keywords: ["*PPSAPI_WS_WATCH_INFORMATION_EX","PPSAPI_WS_WATCH_INFORMATION_EX","PPSAPI_WS_WATCH_INFORMATION_EX structure pointer [PSAPI]","PSAPI_WS_WATCH_INFORMATION_EX","PSAPI_WS_WATCH_INFORMATION_EX structure [PSAPI]","base.psapi_ws_watch_information_ex","psapi.psapi_ws_watch_information_ex","psapi/PPSAPI_WS_WATCH_INFORMATION_EX","psapi/PSAPI_WS_WATCH_INFORMATION_EX"]
old-location: psapi\psapi_ws_watch_information_ex.htm
tech.root: psapi
ms.assetid: fb0429b1-ec93-401c-aeb1-f7e9d9acfa47
ms.date: 12/05/2018
ms.keywords: '*PPSAPI_WS_WATCH_INFORMATION_EX, PPSAPI_WS_WATCH_INFORMATION_EX, PPSAPI_WS_WATCH_INFORMATION_EX structure pointer [PSAPI], PSAPI_WS_WATCH_INFORMATION_EX, PSAPI_WS_WATCH_INFORMATION_EX structure [PSAPI], base.psapi_ws_watch_information_ex, psapi.psapi_ws_watch_information_ex, psapi/PPSAPI_WS_WATCH_INFORMATION_EX, psapi/PSAPI_WS_WATCH_INFORMATION_EX'
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PSAPI_WS_WATCH_INFORMATION_EX, *PPSAPI_WS_WATCH_INFORMATION_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSAPI_WS_WATCH_INFORMATION_EX
 - psapi/_PSAPI_WS_WATCH_INFORMATION_EX
 - PPSAPI_WS_WATCH_INFORMATION_EX
 - psapi/PPSAPI_WS_WATCH_INFORMATION_EX
 - PSAPI_WS_WATCH_INFORMATION_EX
 - psapi/PSAPI_WS_WATCH_INFORMATION_EX
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
 - PSAPI_WS_WATCH_INFORMATION_EX
---

# PSAPI_WS_WATCH_INFORMATION_EX structure


## -description

Contains extended information about a page added to a process working set.

## -struct-fields

### -field BasicInfo

A <a href="/windows/desktop/api/psapi/ns-psapi-psapi_ws_watch_information">PSAPI_WS_WATCH_INFORMATION</a> structure.

### -field FaultingThreadId

The identifier of the thread that caused the page fault.

### -field Flags

This member is reserved for future use.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-getwschangesex">GetWsChangesEx</a>



<a href="/windows/desktop/api/psapi/ns-psapi-psapi_ws_watch_information">PSAPI_WS_WATCH_INFORMATION</a>