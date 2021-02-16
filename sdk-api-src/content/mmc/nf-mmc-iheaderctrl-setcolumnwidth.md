---
UID: NF:mmc.IHeaderCtrl.SetColumnWidth
title: IHeaderCtrl::SetColumnWidth (mmc.h)
description: Sets the width, in pixels, of a specific column.
helpviewer_keywords: ["IHeaderCtrl interface [MMC]","SetColumnWidth method","IHeaderCtrl.SetColumnWidth","IHeaderCtrl::SetColumnWidth","MMCLV_AUTO","SetColumnWidth","SetColumnWidth method [MMC]","SetColumnWidth method [MMC]","IHeaderCtrl interface","mmc.iheaderctrl_setcolumnwidth","mmc/IHeaderCtrl::SetColumnWidth"]
old-location: mmc\iheaderctrl_setcolumnwidth.htm
tech.root: mmc
ms.assetid: E704FF35-3859-4313-B42D-77A114AA6E78
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl interface [MMC],SetColumnWidth method, IHeaderCtrl.SetColumnWidth, IHeaderCtrl::SetColumnWidth, MMCLV_AUTO, SetColumnWidth, SetColumnWidth method [MMC], SetColumnWidth method [MMC],IHeaderCtrl interface, mmc.iheaderctrl_setcolumnwidth, mmc/IHeaderCtrl::SetColumnWidth
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
 - IHeaderCtrl::SetColumnWidth
 - mmc/IHeaderCtrl::SetColumnWidth
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
 - IHeaderCtrl.SetColumnWidth
---

# IHeaderCtrl::SetColumnWidth


## -description

Sets the width, in pixels, of a specific column.

## -parameters

### -param nCol [in]

A zero-based index that specifies the location of the column relative to other columns in the result pane.

### -param nWidth [in]

A value that specifies the width of the column. This value must be in pixels, or it can be the following value:



#### MMCLV_AUTO

MMC automatically determines the width of the column based on the width of the text in the column title.

## -returns

This method can return one of these values.

## -remarks

MMC does not persist in memory any changes made to a column set due to the action of <b>IHeaderCtrl::SetColumnWidth</b>, so snap-ins must update persisted column configuration data after modifying the width of columns in a column set. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/iheaderctrl2-and-column-persistence">IHeaderCtrl2 and Column Persistence</a>.

The HIDE_COLUMN flag for the nWidth parameter is not supported for 
SetColumnWidth. If the snap-in must hide the column, it must call <a href="/windows/desktop/api/mmc/nf-mmc-iconsole-selectscopeitem">IConsole::SelectScopeItem</a> to reselect the scope item and then in the resulting call to the snap-in's <a href="/previous-versions/windows/desktop/mmc/mmcn-show">MMCN_SHOW</a> notification handler, it must use nWidth=HIDE_COLUMN when inserting the column (in the call to <a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl-insertcolumn">IHeaderCtrl::InsertColumn</a>).

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iheaderctrl">IHeaderCtrl</a>



<a href="/previous-versions/windows/desktop/mmc/iheaderctrl2-and-column-persistence">IHeaderCtrl2 and Column Persistence</a>