---
UID: NF:mmc.IResultData.SetViewMode
title: IResultData::SetViewMode (mmc.h)
description: Enables the snap-in to set the view mode in which the result view pane displays its items.
helpviewer_keywords: ["IResultData interface [MMC]","SetViewMode method","IResultData.SetViewMode","IResultData2 interface [MMC]","SetViewMode method","IResultData2::SetViewMode","IResultData::SetViewMode","MMCLV_VIEWSTYLE_FILTERED","MMCLV_VIEWSTYLE_ICON","MMCLV_VIEWSTYLE_LIST","MMCLV_VIEWSTYLE_REPORT","MMCLV_VIEWSTYLE_SMALLICON","SetViewMode","SetViewMode method [MMC]","SetViewMode method [MMC]","IResultData interface","SetViewMode method [MMC]","IResultData2 interface","_slate_iresultdata_setviewmode","mmc.iresultdata_setviewmode","mmc/IResultData2::SetViewMode","mmc/IResultData::SetViewMode"]
old-location: mmc\iresultdata_setviewmode.htm
tech.root: mmc
ms.assetid: 17cff5e6-9624-4873-baa8-96c05d877764
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],SetViewMode method, IResultData.SetViewMode, IResultData2 interface [MMC],SetViewMode method, IResultData2::SetViewMode, IResultData::SetViewMode, MMCLV_VIEWSTYLE_FILTERED, MMCLV_VIEWSTYLE_ICON, MMCLV_VIEWSTYLE_LIST, MMCLV_VIEWSTYLE_REPORT, MMCLV_VIEWSTYLE_SMALLICON, SetViewMode, SetViewMode method [MMC], SetViewMode method [MMC],IResultData interface, SetViewMode method [MMC],IResultData2 interface, _slate_iresultdata_setviewmode, mmc.iresultdata_setviewmode, mmc/IResultData2::SetViewMode, mmc/IResultData::SetViewMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResultData::SetViewMode
 - mmc/IResultData::SetViewMode
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
 - IResultData.SetViewMode
 - IResultData2.SetViewMode
---

# IResultData::SetViewMode


## -description

The <b>IResultData::SetViewMode</b> method enables the snap-in to set the view mode in which the result view pane displays its items. Be aware that view modes apply only to list views.

## -parameters

### -param lViewMode [in]

A value that specifies the view mode to be set in the result pane. It can be one of the following values:



#### MMCLV_VIEWSTYLE_ICON

Items are displayed as title strings under their large (32x32) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_REPORT

Items are displayed as title strings to the right of their small (16x16) icon representations. Items are tabulated under the header in the zero position of the zero-based index on the left side of the result view pane. Subsequent headers are produced from left to right and corresponding subitems are placed beneath each. To enter the report mode, you must have already called 
<a href="/previous-versions/windows/desktop/legacy/aa814793(v=vs.85)">IConsole::SetHeader</a>.



#### MMCLV_VIEWSTYLE_SMALLICON

Items are displayed as title strings under their small (16x16) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_LIST

Items are displayed as title strings to the right of their small (16x16) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_FILTERED

Allows a snap-in to programmatically set the view mode to filtered view. For more information about filtered views, see 
<a href="/previous-versions/windows/desktop/mmc/adding-filtered-views">Adding Filtered Views</a>.

This parameter must not be <b>NULL</b>.

## -returns

This method can return one of these values.

## -remarks

This method provides the same functionality for both virtual and non-virtual list views. For more information about a scenario where you could use <b>IResultData::SetViewMode</b>, see 
<a href="/previous-versions/windows/desktop/mmc/using-list-views-implementation-details">Using List Views: Implementation Details</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-getviewmode">IResultData::GetViewMode</a>