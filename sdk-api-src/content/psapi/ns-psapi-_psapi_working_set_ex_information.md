---
UID: NS:psapi._PSAPI_WORKING_SET_EX_INFORMATION
title: "_PSAPI_WORKING_SET_EX_INFORMATION"
author: windows-driver-content
description: Contains extended working set information for a process.
old-location: psapi\psapi_working_set_ex_information.htm
old-project: psapi
ms.assetid: d3500737-b9af-41a8-bf69-61d0bfbd6ce4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PPSAPI_WORKING_SET_EX_INFORMATION, PPSAPI_WORKING_SET_EX_INFORMATION, PPSAPI_WORKING_SET_EX_INFORMATION structure pointer [PSAPI], PSAPI_WORKING_SET_EX_INFORMATION, PSAPI_WORKING_SET_EX_INFORMATION structure [PSAPI], _PSAPI_WORKING_SET_EX_INFORMATION, base.psapi_working_set_ex_information, psapi.psapi_working_set_ex_information, psapi/PPSAPI_WORKING_SET_EX_INFORMATION, psapi/PSAPI_WORKING_SET_EX_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PSAPI_WORKING_SET_EX_INFORMATION, *PPSAPI_WORKING_SET_EX_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Psapi.h
api_name:
-	PSAPI_WORKING_SET_EX_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _PSAPI_WORKING_SET_EX_INFORMATION structure


## -description


Contains extended working set information for a process.


## -struct-fields




### -field VirtualAddress

The virtual address.


### -field VirtualAttributes

A <a href="https://msdn.microsoft.com/4ba17fa0-2aed-4099-9380-fc13f1b826ca">PSAPI_WORKING_SET_EX_BLOCK</a> union that indicates the attributes of the page at <b>VirtualAddress</b>.


## -see-also




<a href="https://msdn.microsoft.com/4ba17fa0-2aed-4099-9380-fc13f1b826ca">PSAPI_WORKING_SET_EX_BLOCK</a>



<a href="https://msdn.microsoft.com/59ae76c9-e954-4648-9c9f-787136375b02">QueryWorkingSetEx</a>
 

 

