---
UID: NS:pdh._PDH_DATA_ITEM_PATH_ELEMENTS_A
title: PDH_DATA_ITEM_PATH_ELEMENTS_A (pdh.h)
description: The PDH_DATA_ITEM_PATH_ELEMENTS structure contains the path elements of a specific data item. (ANSI)
helpviewer_keywords: ["*PPDH_DATA_ITEM_PATH_ELEMENTS_A","PDH_DATA_ITEM_PATH_ELEMENTS","PDH_DATA_ITEM_PATH_ELEMENTS structure [Perf]","PDH_DATA_ITEM_PATH_ELEMENTS_A","PDH_DATA_ITEM_PATH_ELEMENTS_W","_win32_pdh_data_item_path_elements_str","base.pdh_data_item_path_elements_str","pdh/PDH_DATA_ITEM_PATH_ELEMENTS","pdh/PDH_DATA_ITEM_PATH_ELEMENTS_A","pdh/PDH_DATA_ITEM_PATH_ELEMENTS_W","perf.pdh_data_item_path_elements_str"]
old-location: perf\pdh_data_item_path_elements_str.htm
tech.root: perf
ms.assetid: 7d80d9ac-0123-4743-93a2-fa9d609d81b2
ms.date: 12/05/2018
ms.keywords: '*PPDH_DATA_ITEM_PATH_ELEMENTS_A, PDH_DATA_ITEM_PATH_ELEMENTS, PDH_DATA_ITEM_PATH_ELEMENTS structure [Perf], PDH_DATA_ITEM_PATH_ELEMENTS_A, PDH_DATA_ITEM_PATH_ELEMENTS_W, _win32_pdh_data_item_path_elements_str, base.pdh_data_item_path_elements_str, pdh/PDH_DATA_ITEM_PATH_ELEMENTS, pdh/PDH_DATA_ITEM_PATH_ELEMENTS_A, pdh/PDH_DATA_ITEM_PATH_ELEMENTS_W, perf.pdh_data_item_path_elements_str'
req.header: pdh.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PDH_DATA_ITEM_PATH_ELEMENTS_A, *PPDH_DATA_ITEM_PATH_ELEMENTS_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_DATA_ITEM_PATH_ELEMENTS_A
 - pdh/_PDH_DATA_ITEM_PATH_ELEMENTS_A
 - PPDH_DATA_ITEM_PATH_ELEMENTS_A
 - pdh/PPDH_DATA_ITEM_PATH_ELEMENTS_A
 - PDH_DATA_ITEM_PATH_ELEMENTS_A
 - pdh/PDH_DATA_ITEM_PATH_ELEMENTS_A
dev_langs:
 - c++
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
---

# PDH_DATA_ITEM_PATH_ELEMENTS_A structure


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

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_info_a">PDH_COUNTER_INFO</a>
