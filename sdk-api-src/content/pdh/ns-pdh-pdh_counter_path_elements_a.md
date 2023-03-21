---
UID: NS:pdh._PDH_COUNTER_PATH_ELEMENTS_A
title: PDH_COUNTER_PATH_ELEMENTS_A (pdh.h)
description: The PDH_COUNTER_PATH_ELEMENTS structure contains the components of a counter path. (ANSI)
helpviewer_keywords: ["*PPDH_COUNTER_PATH_ELEMENTS_A","PDH_COUNTER_PATH_ELEMENTS","PDH_COUNTER_PATH_ELEMENTS structure [Perf]","PDH_COUNTER_PATH_ELEMENTS_A","PDH_COUNTER_PATH_ELEMENTS_W","PPDH_COUNTER_PATH_ELEMENTS","PPDH_COUNTER_PATH_ELEMENTS structure pointer [Perf]","_win32_pdh_counter_path_elements_str","base.pdh_counter_path_elements_str","pdh/PDH_COUNTER_PATH_ELEMENTS","pdh/PDH_COUNTER_PATH_ELEMENTS_A","pdh/PDH_COUNTER_PATH_ELEMENTS_W","pdh/PPDH_COUNTER_PATH_ELEMENTS","perf.pdh_counter_path_elements_str"]
old-location: perf\pdh_counter_path_elements_str.htm
tech.root: perf
ms.assetid: ffa2a076-7267-406b-8eed-4a49504a7ad6
ms.date: 12/05/2018
ms.keywords: '*PPDH_COUNTER_PATH_ELEMENTS_A, PDH_COUNTER_PATH_ELEMENTS, PDH_COUNTER_PATH_ELEMENTS structure [Perf], PDH_COUNTER_PATH_ELEMENTS_A, PDH_COUNTER_PATH_ELEMENTS_W, PPDH_COUNTER_PATH_ELEMENTS, PPDH_COUNTER_PATH_ELEMENTS structure pointer [Perf], _win32_pdh_counter_path_elements_str, base.pdh_counter_path_elements_str, pdh/PDH_COUNTER_PATH_ELEMENTS, pdh/PDH_COUNTER_PATH_ELEMENTS_A, pdh/PDH_COUNTER_PATH_ELEMENTS_W, pdh/PPDH_COUNTER_PATH_ELEMENTS, perf.pdh_counter_path_elements_str'
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
targetos: Windows
req.typenames: PDH_COUNTER_PATH_ELEMENTS_A, *PPDH_COUNTER_PATH_ELEMENTS_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_COUNTER_PATH_ELEMENTS_A
 - pdh/_PDH_COUNTER_PATH_ELEMENTS_A
 - PPDH_COUNTER_PATH_ELEMENTS_A
 - pdh/PPDH_COUNTER_PATH_ELEMENTS_A
 - PDH_COUNTER_PATH_ELEMENTS_A
 - pdh/PDH_COUNTER_PATH_ELEMENTS_A
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
 - PDH_COUNTER_PATH_ELEMENTS
 - PDH_COUNTER_PATH_ELEMENTS_A
 - PDH_COUNTER_PATH_ELEMENTS_W
---

# PDH_COUNTER_PATH_ELEMENTS_A structure


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

This structure is used by <a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a> to create a counter path and by <a href="/windows/desktop/api/pdh/nf-pdh-pdhparsecounterpatha">PdhParseCounterPath</a> to parse a counter path.

When you allocate memory for this structure, allocate enough memory for the member strings, such as <b>szCounterName</b>, that are appended to the end of this structure.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhparsecounterpatha">PdhParseCounterPath</a>
