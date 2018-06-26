---
UID: NS:pdh._PDH_RAW_COUNTER_ITEM_W
title: "_PDH_RAW_COUNTER_ITEM_W"
author: windows-sdk-content
description: The PDH_RAW_COUNTER_ITEM structure contains the instance name and raw value of a counter.
old-location: perf\pdh_raw_counter_item_str.htm
old-project: PerfCtrs
ms.assetid: 602e0d44-3551-4a26-a5b7-8f7015131f9a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PPDH_RAW_COUNTER_ITEM_W, PDH_RAW_COUNTER_ITEM, PDH_RAW_COUNTER_ITEM structure [Perf], PDH_RAW_COUNTER_ITEM,*PPDH_RAW_COUNTER_ITEM, PDH_RAW_COUNTER_ITEM,*PPDH_RAW_COUNTER_ITEM structure [Perf], PDH_RAW_COUNTER_ITEM_A, PDH_RAW_COUNTER_ITEM_W, _PDH_RAW_COUNTER_ITEM_W, _win32_pdh_raw_counter_item_str, base.pdh_raw_counter_item_str, pdh/PDH_RAW_COUNTER_ITEM, pdh/PDH_RAW_COUNTER_ITEM_A, pdh/PDH_RAW_COUNTER_ITEM_W, perf.pdh_raw_counter_item_str"
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
req.unicode-ansi: PDH_RAW_COUNTER_ITEM_W (Unicode) and PDH_RAW_COUNTER_ITEM_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDH_RAW_COUNTER_ITEM_W, *PPDH_RAW_COUNTER_ITEM_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_RAW_COUNTER_ITEM, *PPDH_RAW_COUNTER_ITEM
 - PDH_RAW_COUNTER_ITEM_A
 - PDH_RAW_COUNTER_ITEM_W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PDH_RAW_COUNTER_ITEM_W structure


## -description



			The 
<b>PDH_RAW_COUNTER_ITEM</b> structure contains the instance name and raw value of a counter.
		


## -struct-fields




### -field szName

Pointer to a null-terminated string that specifies the instance name of the counter. The string is appended to the end of this structure.


### -field RawValue

 A <a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a> structure that contains the raw counter value of the instance.


## -see-also




<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>



<a href="https://msdn.microsoft.com/03b30d08-6901-45cd-bd6d-d2672eb0f914">PdhGetRawCounterArray</a>
 

 

