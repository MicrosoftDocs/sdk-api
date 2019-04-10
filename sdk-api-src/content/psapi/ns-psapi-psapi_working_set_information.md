---
UID: NS:psapi._PSAPI_WORKING_SET_INFORMATION
title: PSAPI_WORKING_SET_INFORMATION (psapi.h)
author: windows-sdk-content
description: Contains working set information for a process.
old-location: psapi\psapi_working_set_information.htm
tech.root: psapi
ms.assetid: 59ca42c0-ca88-4153-b061-980d961a8ca2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPSAPI_WORKING_SET_INFORMATION, PPSAPI_WORKING_SET_INFORMATION, PPSAPI_WORKING_SET_INFORMATION structure pointer [PSAPI], PSAPI_WORKING_SET_INFORMATION, PSAPI_WORKING_SET_INFORMATION structure [PSAPI], base.psapi_working_set_information, psapi.psapi_working_set_information, psapi/PPSAPI_WORKING_SET_INFORMATION, psapi/PSAPI_WORKING_SET_INFORMATION"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - PSAPI_WORKING_SET_INFORMATION
product: Windows
targetos: Windows
req.typenames: PSAPI_WORKING_SET_INFORMATION, *PPSAPI_WORKING_SET_INFORMATION
req.redist: 
---

# PSAPI_WORKING_SET_INFORMATION structure


## -description


Contains working set information for a process.


## -struct-fields




### -field NumberOfEntries

The number of entries in the <b>WorkingSetInfo</b> array.


### -field WorkingSetInfo

An array of <a href="https://msdn.microsoft.com/feb64235-1003-4595-a6a9-aca1f94f94b8">PSAPI_WORKING_SET_BLOCK</a> elements, one for each page in the process working set.


## -see-also




<a href="https://msdn.microsoft.com/feb64235-1003-4595-a6a9-aca1f94f94b8">PSAPI_WORKING_SET_BLOCK</a>



<a href="https://msdn.microsoft.com/b932153f-2bbd-460e-8ff7-b3e493c397bb">QueryWorkingSet</a>
 

 

