---
UID: NS:psapi._PSAPI_WS_WATCH_INFORMATION
title: "_PSAPI_WS_WATCH_INFORMATION"
author: windows-sdk-content
description: Contains information about a page added to a process working set.
old-location: psapi\psapi_ws_watch_information_str.htm
old-project: psapi
ms.assetid: 61083366-2a55-431c-807a-3eb85ba0b347
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PPSAPI_WS_WATCH_INFORMATION, PPSAPI_WS_WATCH_INFORMATION, PPSAPI_WS_WATCH_INFORMATION structure pointer [PSAPI], PSAPI_WS_WATCH_INFORMATION, PSAPI_WS_WATCH_INFORMATION structure [PSAPI], _PSAPI_WS_WATCH_INFORMATION, _win32_psapi_ws_watch_information_str, base.psapi_ws_watch_information_str, psapi.psapi_ws_watch_information_str, psapi/PPSAPI_WS_WATCH_INFORMATION, psapi/PSAPI_WS_WATCH_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: psapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PSAPI_WS_WATCH_INFORMATION, *PPSAPI_WS_WATCH_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - PSAPI_WS_WATCH_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PSAPI_WS_WATCH_INFORMATION structure


## -description


Contains information about a page added to a process working set.


## -struct-fields




### -field FaultingPc

A pointer to the instruction that caused the page fault.


### -field FaultingVa

A pointer to the page that was added to the working set.


## -see-also




<a href="https://msdn.microsoft.com/ace5106c-9c7b-4d5f-a69a-c3a8bff0bb2d">GetWsChanges</a>
 

 

