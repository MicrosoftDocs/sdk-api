---
UID: NS:pdh._PDH_COUNTER_PATH_ELEMENTS_A
title: "_PDH_COUNTER_PATH_ELEMENTS_A"
author: windows-sdk-content
description: The PDH_COUNTER_PATH_ELEMENTS structure contains the components of a counter path.
old-location: perf\pdh_counter_path_elements_str.htm
tech.root: PerfCtrs
ms.assetid: ffa2a076-7267-406b-8eed-4a49504a7ad6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PPDH_COUNTER_PATH_ELEMENTS_A, PDH_COUNTER_PATH_ELEMENTS, PDH_COUNTER_PATH_ELEMENTS structure [Perf], PDH_COUNTER_PATH_ELEMENTS_A, PDH_COUNTER_PATH_ELEMENTS_W, PPDH_COUNTER_PATH_ELEMENTS, PPDH_COUNTER_PATH_ELEMENTS structure pointer [Perf], _PDH_COUNTER_PATH_ELEMENTS_A, _win32_pdh_counter_path_elements_str, base.pdh_counter_path_elements_str, pdh/PDH_COUNTER_PATH_ELEMENTS, pdh/PDH_COUNTER_PATH_ELEMENTS_A, pdh/PDH_COUNTER_PATH_ELEMENTS_W, pdh/PPDH_COUNTER_PATH_ELEMENTS, perf.pdh_counter_path_elements_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PDH_COUNTER_PATH_ELEMENTS_W (Unicode) and PDH_COUNTER_PATH_ELEMENTS_A (ANSI)
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
 - Pdh.h
api_name:
 - PDH_COUNTER_PATH_ELEMENTS
 - PDH_COUNTER_PATH_ELEMENTS_A
 - PDH_COUNTER_PATH_ELEMENTS_W
product: Windows
targetos: Windows
req.typenames: PDH_COUNTER_PATH_ELEMENTS_A, *PPDH_COUNTER_PATH_ELEMENTS_A
req.redist: 
---

# _PDH_COUNTER_PATH_ELEMENTS_A structure


## -description


The 
<b>PDH_COUNTER_PATH_ELEMENTS</b> structure contains the components of a counter path. 


## -struct-fields




### -field szMachineName

Pointer to a null-terminated string that specifies the computer name. 


### -field szObjectName

Pointer to a null-terminated string that specifies the object name.


### -field szInstanceName

Pointer to a null-terminated string that specifies the instance name. Can contain a wildcard character.


### -field szParentInstance

Pointer to a null-terminated string that specifies the parent instance name. Can contain a wildcard character.


### -field dwInstanceIndex

Index used to uniquely identify duplicate instance names.


### -field szCounterName

Pointer to a null-terminated string that specifies the counter name.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a> to create a counter path and by <a href="https://msdn.microsoft.com/760b94e9-88df-4f7d-92e9-333d682779f6">PdhParseCounterPath</a> to parse a counter path.

When you allocate memory for this structure, allocate enough memory for the member strings, such as <b>szCounterName</b>, that are appended to the end of this structure.




## -see-also




<a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a>



<a href="https://msdn.microsoft.com/760b94e9-88df-4f7d-92e9-333d682779f6">PdhParseCounterPath</a>
 

 

