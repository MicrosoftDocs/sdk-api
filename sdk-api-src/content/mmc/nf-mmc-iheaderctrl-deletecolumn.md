---
UID: NF:mmc.IHeaderCtrl.DeleteColumn
title: IHeaderCtrl::DeleteColumn (mmc.h)
description: Removes a column from the header of the result view.
helpviewer_keywords: ["DeleteColumn","DeleteColumn method [MMC]","DeleteColumn method [MMC]","IHeaderCtrl interface","IHeaderCtrl interface [MMC]","DeleteColumn method","IHeaderCtrl.DeleteColumn","IHeaderCtrl::DeleteColumn","mmc.iheaderctrl_deletecolumn","mmc/IHeaderCtrl::DeleteColumn"]
old-location: mmc\iheaderctrl_deletecolumn.htm
tech.root: mmc
ms.assetid: 85A4D929-E98B-4C84-9E5C-EA5E41BD0D07
ms.date: 12/05/2018
ms.keywords: DeleteColumn, DeleteColumn method [MMC], DeleteColumn method [MMC],IHeaderCtrl interface, IHeaderCtrl interface [MMC],DeleteColumn method, IHeaderCtrl.DeleteColumn, IHeaderCtrl::DeleteColumn, mmc.iheaderctrl_deletecolumn, mmc/IHeaderCtrl::DeleteColumn
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHeaderCtrl::DeleteColumn
 - mmc/IHeaderCtrl::DeleteColumn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IHeaderCtrl.DeleteColumn
---

# IHeaderCtrl::DeleteColumn


## -description

Removes a column from the header of the result view.

## -parameters

### -param nCol [in]

A zero-based index that identifies the column to be removed.

## -returns

This method can return one of these values.

## -remarks

If a column is removed, all columns with indexes greater than the one removed are adjusted down by one.

MMC does not persist in memory any changes made to a column set due to the action of <b>IHeaderCtrl::DeleteColumn</b>, so snap-ins must update persisted column configuration data after deleting columns from a column set. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/iheaderctrl2-and-column-persistence">IHeaderCtrl2 and Column Persistence</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method returns <i>E_FAIL</i> when an item has already been inserted into the result view.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iheaderctrl">IHeaderCtrl</a>



<a href="/previous-versions/windows/desktop/mmc/iheaderctrl2-and-column-persistence">IHeaderCtrl2 and Column Persistence</a>