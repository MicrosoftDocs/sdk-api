---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SSortOrder structure


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

TABLE_SORT_COMBINE can only be used when the <b>SSortOrder</b> structure is being used as an entry in an <a href="https://msdn.microsoft.com/1e209a0a-69ac-4705-9c24-0e3f2d8c4896">SSortOrderSet</a> structure to specify multiple sort orders for a categorized sort. TABLE_SORT_COMBINE cannot be used in the first <b>SSortOrder</b> structure in an <b>SSortOrderSet</b> structure.



#### TABLE_SORT_DESCEND

Table is sorted in descending order.

