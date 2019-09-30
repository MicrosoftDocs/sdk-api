---
UID: NN:mmc.IColumnData
title: IColumnData (mmc.h)
author: windows-sdk-content
description: The IColumnData interface is introduced in MMC 1.2.
old-location: mmc\icolumndata.htm
tech.root: mmc
ms.assetid: fb2b8863-c476-4997-915d-329cf66fd945
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IColumnData, IColumnData interface [MMC], IColumnData interface [MMC],described, _slate_icolumndata, mmc.icolumndata, mmc/IColumnData
ms.topic: interface
f1_keywords: 
 - "mmc/IColumnData"
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IColumnData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IColumnData interface


## -description


The 
<b>IColumnData</b> interface is introduced in MMC 1.2.

The 
<b>IColumnData</b> interface enables a snap-in to set and retrieve the persisted view data of list view columns to use for column customization. For more information about when to use the 
<b>IColumnData</b> interface, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-icolumndata">Using IColumnData</a>.

The interface provides methods for programmatically providing the same functionality that MMC provides in the <b>Modify Columns</b> dialog box. In addition, the 
<b>IColumnData</b> interface provides methods for setting and retrieving the sorted column and sort direction of a particular column set.

All data set and retrieved by the methods of the 
<b>IColumnData</b> interface is persisted by MMC in memory, and not in a stream or storage medium. This data is persisted to an .msc console file only when the user chooses the 
<b>Save</b> menu command.

MMC persists column data (also called column configuration data) per column set (using a column set ID) per view per snap-in instance. Within each view, each column set ID references its own column configuration data. The snap-in can use the 
<b>IColumnData</b> interface pertaining to the particular view to access the column configuration data of that view.

For more information about column customization, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>.

The 
<b>IColumnData</b> interface can be queried from the IConsole passed into 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponent::Initialize</a> during the component creation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IColumnData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IColumnData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IColumnData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icolumndata-getcolumnconfigdata">GetColumnConfigData</a>
</td>
<td align="left" width="63%">
Retrieves the width, order, and hidden status of columns in a column set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icolumndata-getcolumnsortdata">GetColumnSortData</a>
</td>
<td align="left" width="63%">
Retrieves the sorting direction for columns in a column set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icolumndata-setcolumnconfigdata">SetColumnConfigData</a>
</td>
<td align="left" width="63%">
Sets the width, order, and hidden status of columns in a column set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icolumndata-setcolumnsortdata">SetColumnSortData</a>
</td>
<td align="left" width="63%">
Sets the sorting direction for columns in a column set.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-icolumndata">Using IColumnData</a>
 

 

