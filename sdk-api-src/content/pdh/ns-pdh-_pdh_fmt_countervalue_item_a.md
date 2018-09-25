---
UID: NS:pdh._PDH_FMT_COUNTERVALUE_ITEM_A
title: "_PDH_FMT_COUNTERVALUE_ITEM_A"
author: windows-sdk-content
description: The PDH_FMT_COUNTERVALUE_ITEM structure contains the instance name and formatted value of a counter.
old-location: perf\pdh_fmt_countervalue_item_str.htm
tech.root: perfctrs
ms.assetid: d3bc6ad3-0cab-4843-ae1d-5f384948a1ea
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PPDH_FMT_COUNTERVALUE_ITEM_A, PDH_FMT_COUNTERVALUE_ITEM, PDH_FMT_COUNTERVALUE_ITEM structure [Perf], PDH_FMT_COUNTERVALUE_ITEM_A, PDH_FMT_COUNTERVALUE_ITEM_W, PPDH_FMT_COUNTERVALUE_ITEM, PPDH_FMT_COUNTERVALUE_ITEM structure pointer [Perf], _PDH_FMT_COUNTERVALUE_ITEM_A, _win32_pdh_fmt_countervalue_item_str, base.pdh_fmt_countervalue_item_str, pdh/PDH_FMT_COUNTERVALUE_ITEM, pdh/PDH_FMT_COUNTERVALUE_ITEM_A, pdh/PDH_FMT_COUNTERVALUE_ITEM_W, pdh/PPDH_FMT_COUNTERVALUE_ITEM, perf.pdh_fmt_countervalue_item_str"
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
req.unicode-ansi: PDH_FMT_COUNTERVALUE_ITEM_W (Unicode) and PDH_FMT_COUNTERVALUE_ITEM_A (ANSI)
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
 - PDH_FMT_COUNTERVALUE_ITEM
 - PDH_FMT_COUNTERVALUE_ITEM_A
 - PDH_FMT_COUNTERVALUE_ITEM_W
product: Windows
targetos: Windows
req.typenames: PDH_FMT_COUNTERVALUE_ITEM_A, *PPDH_FMT_COUNTERVALUE_ITEM_A
req.redist: 
---

# _PDH_FMT_COUNTERVALUE_ITEM_A structure


## -description


The 
<b>PDH_FMT_COUNTERVALUE_ITEM</b> structure contains the instance name and formatted value of a counter.
		


## -struct-fields




### -field szName

Pointer to a null-terminated string that specifies the instance name of the counter. The string is appended to the end of this structure.


### -field FmtValue

 A <a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a> structure that contains the counter value of the instance.


## -see-also




<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a>



<a href="https://msdn.microsoft.com/0f388c7e-d0c8-461d-908c-48af92166996">PdhGetFormattedCounterArray</a>
 

 

