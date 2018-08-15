---
UID: NF:mmcobj.Column.SetAsSortColumn
title: Column::SetAsSortColumn
author: windows-sdk-content
description: The SetAsSortColumn method specifies the sort order for the column.
old-location: mmc\column_setassortcolumn.htm
old-project: MMC
ms.assetid: dbbf6c9c-ba58-4588-b972-7d9b2029ee91
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Column interface [MMC],SetAsSortColumn method, Column object [MMC],SetAsSortColumn method, Column.SetAsSortColumn, Column::SetAsSortColumn, SetAsSortColumn, SetAsSortColumn method [MMC], SetAsSortColumn method [MMC],Column interface, SetAsSortColumn method [MMC],Column object, SortOrder_Ascending, SortOrder_Descending, _slate_column.setassortcolumn_method, mmc.column_setassortcolumn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MMCObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.exe
api_name:
 - Column.SetAsSortColumn
 - Column.SetAsSortColumn
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# Column::SetAsSortColumn


## -description


The 
<b>SetAsSortColumn</b> method specifies the sort order for the column.


## -parameters




### -param SortOrder

The new sort order being assigned for the column. This can be one of the following 
<a href="https://msdn.microsoft.com/2843c9fc-e422-4c1a-a348-5c6656a160ed">ColumnSortOrder</a> values.



#### SortOrder_Ascending

The column is sorted in ascending order.



#### SortOrder_Descending

The column is sorted in descending order.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/2843c9fc-e422-4c1a-a348-5c6656a160ed">ColumnSortOrder</a>
 

 

