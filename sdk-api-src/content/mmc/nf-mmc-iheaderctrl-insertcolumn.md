---
UID: NF:mmc.IHeaderCtrl.InsertColumn
title: IHeaderCtrl::InsertColumn (mmc.h)
description: Adds a column to a default result pane.
helpviewer_keywords: ["HIDE_COLUMN","IHeaderCtrl interface [MMC]","InsertColumn method","IHeaderCtrl.InsertColumn","IHeaderCtrl::InsertColumn","InsertColumn","InsertColumn method [MMC]","InsertColumn method [MMC]","IHeaderCtrl interface","LVCFMT_CENTER","LVCFMT_LEFT","LVCFMT_RIGHT","MMCLV_AUTO","mmc.iheaderctrl_insertcolumn","mmc/IHeaderCtrl::InsertColumn"]
old-location: mmc\iheaderctrl_insertcolumn.htm
tech.root: mmc
ms.assetid: F5499550-9460-4BF9-AF99-F4BDC7F32EBC
ms.date: 12/05/2018
ms.keywords: HIDE_COLUMN, IHeaderCtrl interface [MMC],InsertColumn method, IHeaderCtrl.InsertColumn, IHeaderCtrl::InsertColumn, InsertColumn, InsertColumn method [MMC], InsertColumn method [MMC],IHeaderCtrl interface, LVCFMT_CENTER, LVCFMT_LEFT, LVCFMT_RIGHT, MMCLV_AUTO, mmc.iheaderctrl_insertcolumn, mmc/IHeaderCtrl::InsertColumn
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
 - IHeaderCtrl::InsertColumn
 - mmc/IHeaderCtrl::InsertColumn
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
 - IHeaderCtrl.InsertColumn
---

# IHeaderCtrl::InsertColumn


## -description

Adds a column to a default result pane.

## -parameters

### -param nCol [in]

A zero-based index of the column being inserted.

### -param title [in]

A value that specifies the string that represents the title of the column being inserted. This string can have  a maximum length of <b>MAX_PATH</b> characters.

### -param nFormat [in]

A value that specifies the position of text within the column. For column zero, <i>nFormat</i> must be <b>LVCFMT_LEFT</b>. This value must be one of the following:



#### LVCFMT_LEFT

Text is left-aligned.



#### LVCFMT_CENTER

Text is center-aligned.



#### LVCFMT_RIGHT

Text is right-aligned.

<div class="alert"><b>Note</b>  To use the <b>LVCFMT_*</b> constants, include CommCtrl.h in your source file.</div>
<div> </div>

### -param nWidth [in]

A value that specifies the width of the column in pixels. This value must be one of the following:



#### MMCLV_AUTO

MMC automatically determines the width of the column based on its title string.



#### HIDE_COLUMN

Introduced in MMC 1.2. The column is inserted, but it is hidden. Be aware that the user can make the column visible when 
<a href="/previous-versions/windows/desktop/mmc/how-column-configuration-data-is-used">customizing a list view</a>.

For snap-ins built with the MMC 1.2 SDK, but which are loaded in an older version of MMC, <b>HIDE_COLUMN</b> is interpreted as a zero width. The user can widen the column by dragging it with the mouse.

## -returns

This method can return one of these values.

## -remarks

MMC does not persist in memory any changes made to a column set due to the action of <b>IHeaderCtrl::InsertColumn</b>, so snap-ins must update persisted column configuration data after inserting columns into a column set. See 
<a href="/previous-versions/windows/desktop/mmc/iheaderctrl2-and-column-persistence">IHeaderCtrl2 and Column Persistence</a> for more information.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to 
<b>InsertColumn</b> fail if any items have already been inserted into the result view.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iheaderctrl">IHeaderCtrl</a>



<a href="/previous-versions/windows/desktop/mmc/iheaderctrl2-and-column-persistence">IHeaderCtrl2 and Column Persistence</a>