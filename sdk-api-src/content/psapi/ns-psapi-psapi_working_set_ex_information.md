---
UID: NS:psapi._PSAPI_WORKING_SET_EX_INFORMATION
title: PSAPI_WORKING_SET_EX_INFORMATION (psapi.h)
description: Contains extended working set information for a process.
helpviewer_keywords: ["*PPSAPI_WORKING_SET_EX_INFORMATION","PPSAPI_WORKING_SET_EX_INFORMATION","PPSAPI_WORKING_SET_EX_INFORMATION structure pointer [PSAPI]","PSAPI_WORKING_SET_EX_INFORMATION","PSAPI_WORKING_SET_EX_INFORMATION structure [PSAPI]","base.psapi_working_set_ex_information","psapi.psapi_working_set_ex_information","psapi/PPSAPI_WORKING_SET_EX_INFORMATION","psapi/PSAPI_WORKING_SET_EX_INFORMATION"]
old-location: psapi\psapi_working_set_ex_information.htm
tech.root: psapi
ms.assetid: d3500737-b9af-41a8-bf69-61d0bfbd6ce4
ms.date: 12/05/2018
ms.keywords: '*PPSAPI_WORKING_SET_EX_INFORMATION, PPSAPI_WORKING_SET_EX_INFORMATION, PPSAPI_WORKING_SET_EX_INFORMATION structure pointer [PSAPI], PSAPI_WORKING_SET_EX_INFORMATION, PSAPI_WORKING_SET_EX_INFORMATION structure [PSAPI], base.psapi_working_set_ex_information, psapi.psapi_working_set_ex_information, psapi/PPSAPI_WORKING_SET_EX_INFORMATION, psapi/PSAPI_WORKING_SET_EX_INFORMATION'
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: PSAPI_WORKING_SET_EX_INFORMATION, *PPSAPI_WORKING_SET_EX_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSAPI_WORKING_SET_EX_INFORMATION
 - psapi/_PSAPI_WORKING_SET_EX_INFORMATION
 - PPSAPI_WORKING_SET_EX_INFORMATION
 - psapi/PPSAPI_WORKING_SET_EX_INFORMATION
 - PSAPI_WORKING_SET_EX_INFORMATION
 - psapi/PSAPI_WORKING_SET_EX_INFORMATION
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
 - PSAPI_WORKING_SET_EX_INFORMATION
---

# PSAPI_WORKING_SET_EX_INFORMATION structure


## -description

Contains extended working set information for a process.

## -struct-fields

### -field VirtualAddress

The virtual address.

### -field VirtualAttributes

A <a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_ex_block">PSAPI_WORKING_SET_EX_BLOCK</a> union that indicates the attributes of the page at <b>VirtualAddress</b>.

## -see-also

<a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_ex_block">PSAPI_WORKING_SET_EX_BLOCK</a>



<a href="/windows/desktop/api/psapi/nf-psapi-queryworkingsetex">QueryWorkingSetEx</a>