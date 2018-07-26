---
UID: NF:mmc.IResultData.GetViewMode
title: IResultData::GetViewMode
author: windows-sdk-content
description: Enables the snap-in to retrieve a view mode for the result view pane.
old-location: mmc\iresultdata_getviewmode.htm
old-project: MMC
ms.assetid: e6c9b3ef-3b12-42c1-9b3b-ad890b8bd05e
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetViewMode, GetViewMode method [MMC], GetViewMode method [MMC],IResultData interface, GetViewMode method [MMC],IResultData2 interface, IResultData interface [MMC],GetViewMode method, IResultData.GetViewMode, IResultData2 interface [MMC],GetViewMode method, IResultData2::GetViewMode, IResultData::GetViewMode, MMCLV_VIEWSTYLE_FILTERED, MMCLV_VIEWSTYLE_ICON, MMCLV_VIEWSTYLE_LIST, MMCLV_VIEWSTYLE_REPORT, MMCLV_VIEWSTYLE_SMALLICON, _slate_iresultdata_getviewmode, mmc.iresultdata_getviewmode, mmc/IResultData2::GetViewMode, mmc/IResultData::GetViewMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/bca6fbef-d00b-4f25-823e-fff76a96f59d">IConsole::SetHeader</a>.



#### MMCLV_VIEWSTYLE_SMALLICON

Items are displayed as title strings under their small (16x16) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_LIST

Items are displayed as title strings to the right of their small (16x16) icon representations. Subitems and headers are not displayed.



#### MMCLV_VIEWSTYLE_FILTERED

The list view is displayed as a filtered view. Each list view column has an associated column filter. For more information about filtered views, see 
<a href="https://msdn.microsoft.com/4be29e44-7e64-4c2c-820b-26c6cfea0661">Adding Filtered Views</a>.

This parameter must not be <b>NULL</b>.


## -returns



This method can return one of these values.




## -remarks



This method provides the same functionality for both virtual and nonvirtual list views.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>



<a href="https://msdn.microsoft.com/17cff5e6-9624-4873-baa8-96c05d877764">IResultData::SetViewMode</a>
 

 

