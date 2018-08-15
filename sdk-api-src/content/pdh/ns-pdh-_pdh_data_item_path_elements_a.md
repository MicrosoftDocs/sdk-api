---
UID: NS:pdh._PDH_DATA_ITEM_PATH_ELEMENTS_A
title: "_PDH_DATA_ITEM_PATH_ELEMENTS_A"
author: windows-sdk-content
description: The PDH_DATA_ITEM_PATH_ELEMENTS structure contains the path elements of a specific data item.
old-location: perf\pdh_data_item_path_elements_str.htm
old-project: PerfCtrs
ms.assetid: 7d80d9ac-0123-4743-93a2-fa9d609d81b2
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PPDH_DATA_ITEM_PATH_ELEMENTS_A, PDH_DATA_ITEM_PATH_ELEMENTS, PDH_DATA_ITEM_PATH_ELEMENTS structure [Perf], PDH_DATA_ITEM_PATH_ELEMENTS_A, PDH_DATA_ITEM_PATH_ELEMENTS_W, _PDH_DATA_ITEM_PATH_ELEMENTS_A, _win32_pdh_data_item_path_elements_str, base.pdh_data_item_path_elements_str, pdh/PDH_DATA_ITEM_PATH_ELEMENTS, pdh/PDH_DATA_ITEM_PATH_ELEMENTS_A, pdh/PDH_DATA_ITEM_PATH_ELEMENTS_W, perf.pdh_data_item_path_elements_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: pdh.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PDH_DATA_ITEM_PATH_ELEMENTS_W (Unicode) and PDH_DATA_ITEM_PATH_ELEMENTS_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDH_DATA_ITEM_PATH_ELEMENTS_A, *PPDH_DATA_ITEM_PATH_ELEMENTS_A
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_DATA_ITEM_PATH_ELEMENTS
 - PDH_DATA_ITEM_PATH_ELEMENTS_A
 - PDH_DATA_ITEM_PATH_ELEMENTS_W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PDH_DATA_ITEM_PATH_ELEMENTS_A structure


## -description


The 
<b>PDH_DATA_ITEM_PATH_ELEMENTS</b> structure contains the path elements of a specific data item.
		


## -struct-fields




### -field szMachineName

Pointer to a null-terminated string that specifies the name of the computer where the data item resides.


### -field ObjectGUID

GUID of the object where the data item resides.


### -field dwItemId

Identifier of the data item.


### -field szInstanceName

Pointer to a null-terminated string that specifies the name of the data item instance.


## -see-also




<a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a>
 

 

