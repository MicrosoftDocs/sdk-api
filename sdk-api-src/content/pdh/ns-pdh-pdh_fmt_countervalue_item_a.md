---
UID: NS:pdh._PDH_FMT_COUNTERVALUE_ITEM_A
title: PDH_FMT_COUNTERVALUE_ITEM_A (pdh.h)
description: The PDH_FMT_COUNTERVALUE_ITEM structure contains the instance name and formatted value of a counter. (ANSI)
helpviewer_keywords: ["*PPDH_FMT_COUNTERVALUE_ITEM_A","PDH_FMT_COUNTERVALUE_ITEM","PDH_FMT_COUNTERVALUE_ITEM structure [Perf]","PDH_FMT_COUNTERVALUE_ITEM_A","PDH_FMT_COUNTERVALUE_ITEM_W","PPDH_FMT_COUNTERVALUE_ITEM","PPDH_FMT_COUNTERVALUE_ITEM structure pointer [Perf]","_win32_pdh_fmt_countervalue_item_str","base.pdh_fmt_countervalue_item_str","pdh/PDH_FMT_COUNTERVALUE_ITEM","pdh/PDH_FMT_COUNTERVALUE_ITEM_A","pdh/PDH_FMT_COUNTERVALUE_ITEM_W","pdh/PPDH_FMT_COUNTERVALUE_ITEM","perf.pdh_fmt_countervalue_item_str"]
old-location: perf\pdh_fmt_countervalue_item_str.htm
tech.root: perf
ms.assetid: d3bc6ad3-0cab-4843-ae1d-5f384948a1ea
ms.date: 12/05/2018
ms.keywords: '*PPDH_FMT_COUNTERVALUE_ITEM_A, PDH_FMT_COUNTERVALUE_ITEM, PDH_FMT_COUNTERVALUE_ITEM structure [Perf], PDH_FMT_COUNTERVALUE_ITEM_A, PDH_FMT_COUNTERVALUE_ITEM_W, PPDH_FMT_COUNTERVALUE_ITEM, PPDH_FMT_COUNTERVALUE_ITEM structure pointer [Perf], _win32_pdh_fmt_countervalue_item_str, base.pdh_fmt_countervalue_item_str, pdh/PDH_FMT_COUNTERVALUE_ITEM, pdh/PDH_FMT_COUNTERVALUE_ITEM_A, pdh/PDH_FMT_COUNTERVALUE_ITEM_W, pdh/PPDH_FMT_COUNTERVALUE_ITEM, perf.pdh_fmt_countervalue_item_str'
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
targetos: Windows
req.typenames: PDH_FMT_COUNTERVALUE_ITEM_A, *PPDH_FMT_COUNTERVALUE_ITEM_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_FMT_COUNTERVALUE_ITEM_A
 - pdh/_PDH_FMT_COUNTERVALUE_ITEM_A
 - PPDH_FMT_COUNTERVALUE_ITEM_A
 - pdh/PPDH_FMT_COUNTERVALUE_ITEM_A
 - PDH_FMT_COUNTERVALUE_ITEM_A
 - pdh/PDH_FMT_COUNTERVALUE_ITEM_A
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
 - PDH_FMT_COUNTERVALUE_ITEM
 - PDH_FMT_COUNTERVALUE_ITEM_A
 - PDH_FMT_COUNTERVALUE_ITEM_W
---

# PDH_FMT_COUNTERVALUE_ITEM_A structure


## -description

The 
<b>PDH_FMT_COUNTERVALUE_ITEM</b> structure contains the instance name and formatted value of a counter.

## -struct-fields

### -field szName

Pointer to a null-terminated string that specifies the instance name of the counter. The string is appended to the end of this structure.

### -field FmtValue

 A <a href="/windows/desktop/api/pdh/ns-pdh-pdh_fmt_countervalue">PDH_FMT_COUNTERVALUE</a> structure that contains the counter value of the instance.

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_fmt_countervalue">PDH_FMT_COUNTERVALUE</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcounterarraya">PdhGetFormattedCounterArray</a>
