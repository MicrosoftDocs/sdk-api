---
UID: NS:wabdefs._SSortOrder
title: SSortOrder (wabdefs.h)
description: Do not use. Defines how to sort rows of a table, describing both the column to use as the sort key and the direction of the sort.
helpviewer_keywords: ["*LPSSortOrder","LPSSortOrder","LPSSortOrder structure pointer [Windows Address Book]","SSortOrder","SSortOrder structure [Windows Address Book]","TABLE_SORT_ASCEND","TABLE_SORT_COMBINE","TABLE_SORT_DESCEND","_wab_SSortOrder","wab._wab_SSortOrder","wabdefs/LPSSortOrder","wabdefs/SSortOrder"]
old-location: wab\_wab_SSortOrder.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\ssortorder.htm
ms.date: 12/05/2018
ms.keywords: '*LPSSortOrder, LPSSortOrder, LPSSortOrder structure pointer [Windows Address Book], SSortOrder, SSortOrder structure [Windows Address Book], TABLE_SORT_ASCEND, TABLE_SORT_COMBINE, TABLE_SORT_DESCEND, _wab_SSortOrder, wab._wab_SSortOrder, wabdefs/LPSSortOrder, wabdefs/SSortOrder'
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SSortOrder, *LPSSortOrder
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SSortOrder
 - wabdefs/_SSortOrder
 - LPSSortOrder
 - wabdefs/LPSSortOrder
 - SSortOrder
 - wabdefs/SSortOrder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SSortOrder
---

# SSortOrder structure


## -description

Do not use. Defines how to sort rows of a table, describing both the column to use as the sort key and the direction of the sort.

## -struct-fields

### -field ulPropTag

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the property tag identifying either the sort key or, for a categorized sort, the category column.

### -field ulOrder

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the order in which the data is to be sorted. The possible values are as follows.



#### TABLE_SORT_ASCEND

Table is sorted in ascending order.



#### TABLE_SORT_COMBINE

Sort operation creates a category that combines the property identified as the sort key column in the <b>ulPropTag</b> member with the sort key column specified in the previous <b>SSortOrder</b> structure.

TABLE_SORT_COMBINE can only be used when the <b>SSortOrder</b> structure is being used as an entry in an <a href="/windows/desktop/api/wabdefs/ns-wabdefs-ssortorderset">SSortOrderSet</a> structure to specify multiple sort orders for a categorized sort. TABLE_SORT_COMBINE cannot be used in the first <b>SSortOrder</b> structure in an <b>SSortOrderSet</b> structure.



#### TABLE_SORT_DESCEND

Table is sorted in descending order.