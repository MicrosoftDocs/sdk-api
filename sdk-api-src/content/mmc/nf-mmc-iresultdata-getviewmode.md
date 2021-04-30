---
UID: NF:mmc.IResultData.GetViewMode
title: IResultData::GetViewMode (mmc.h)
description: Enables the snap-in to retrieve a view mode for the result view pane.
helpviewer_keywords: ["GetViewMode","GetViewMode method [MMC]","GetViewMode method [MMC]","IResultData interface","GetViewMode method [MMC]","IResultData2 interface","IResultData interface [MMC]","GetViewMode method","IResultData.GetViewMode","IResultData2 interface [MMC]","GetViewMode method","IResultData2::GetViewMode","IResultData::GetViewMode","MMCLV_VIEWSTYLE_FILTERED","MMCLV_VIEWSTYLE_ICON","MMCLV_VIEWSTYLE_LIST","MMCLV_VIEWSTYLE_REPORT","MMCLV_VIEWSTYLE_SMALLICON","_slate_iresultdata_getviewmode","mmc.iresultdata_getviewmode","mmc/IResultData2::GetViewMode","mmc/IResultData::GetViewMode"]
old-location: mmc\iresultdata_getviewmode.htm
tech.root: mmc
ms.assetid: e6c9b3ef-3b12-42c1-9b3b-ad890b8bd05e
ms.date: 12/05/2018
ms.keywords: GetViewMode, GetViewMode method [MMC], GetViewMode method [MMC],IResultData interface, GetViewMode method [MMC],IResultData2 interface, IResultData interface [MMC],GetViewMode method, IResultData.GetViewMode, IResultData2 interface [MMC],GetViewMode method, IResultData2::GetViewMode, IResultData::GetViewMode, MMCLV_VIEWSTYLE_FILTERED, MMCLV_VIEWSTYLE_ICON, MMCLV_VIEWSTYLE_LIST, MMCLV_VIEWSTYLE_REPORT, MMCLV_VIEWSTYLE_SMALLICON, _slate_iresultdata_getviewmode, mmc.iresultdata_getviewmode, mmc/IResultData2::GetViewMode, mmc/IResultData::GetViewMode
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
 - IResultData::GetViewMode
 - mmc/IResultData::GetViewMode
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
 - IResultData.GetViewMode
 - IResultData2.GetViewMode
---

# IResultData::GetViewMode


## -description

The <b>IResultData::GetViewMode</b> method enables the snap-in to retrieve a view mode for the result view pane. Be aware that view modes only apply to list views.

## -parameters

### -param lViewMode [out]

A pointer to the view mode to be retrieved. It can be one of the following:



#### MMCLV_VIEWSTYLE_ICON

Items are displayed as title strings under their large (32x32) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_REPORT

Items are displayed as title strings to the right of their small (16x16) icon representations. Items are tabulated under the header in the 0 (zero) position of the zero-based index on the left side of the result view pane. Subsequent headers are produced from left to right and corresponding subitems are placed beneath each. To enter the report mode, you must have already called 
<a href="/previous-versions/windows/desktop/legacy/aa814793(v=vs.85)">IConsole::SetHeader</a>.



#### MMCLV_VIEWSTYLE_SMALLICON

Items are displayed as title strings under their small (16x16) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_LIST

Items are displayed as title strings to the right of their small (16x16) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_FILTERED

The list view is displayed as a filtered view. Each list view column has an associated column filter. For more information about filtered views, see 
<a href="/previous-versions/windows/desktop/mmc/adding-filtered-views">Adding Filtered Views</a>.

This parameter must not be <b>NULL</b>.

## -returns

This method can return one of these values.

## -remarks

This method provides the same functionality for both virtual and nonvirtual list views.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-setviewmode">IResultData::SetViewMode</a>