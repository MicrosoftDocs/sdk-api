---
UID: NE:mmc._MMC_RESULT_VIEW_STYLE
title: "_MMC_RESULT_VIEW_STYLE"
author: windows-sdk-content
description: The MMC_RESULT_VIEW_STYLE enumeration defines the Win32 list view style (LVS_*) flags that can be used to set the view style in the MMC result view pane. They can be used in the add and remove parameters of the IResultData::ModifyViewStyle method.
old-location: mmc\mmc_result_view_style.htm
tech.root: MMC
ms.assetid: 2f1b93e2-aa1d-4478-877b-a26cdb3dc84b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MMC_NOSORTHEADER, MMC_RESULT_VIEW_STYLE, MMC_RESULT_VIEW_STYLE enumeration [MMC], MMC_SHOWSELALWAYS, MMC_SINGLESEL, _MMC_RESULT_VIEW_STYLE, _slate_mmc_result_view_style, mmc.mmc_result_view_style, mmc/MMC_NOSORTHEADER, mmc/MMC_RESULT_VIEW_STYLE, mmc/MMC_SHOWSELALWAYS, mmc/MMC_SINGLESEL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_RESULT_VIEW_STYLE
product: Windows
targetos: Windows
req.typenames: MMC_RESULT_VIEW_STYLE
req.redist: 
---

# _MMC_RESULT_VIEW_STYLE enumeration


## -description


The 
<b>MMC_RESULT_VIEW_STYLE</b> enumeration defines the Win32 list view style (LVS_*) flags that can be used to set the view style in the MMC result view pane. They can be used in the <i>add</i> and <i>remove</i> parameters of the 
<a href="https://msdn.microsoft.com/f33a427c-6952-4877-bbfb-09ac976ea188">IResultData::ModifyViewStyle</a> method.


## -enum-fields




### -field MMC_SINGLESEL

Allows only one item at a time to be selected. Without this view style, multiple items can be selected.


### -field MMC_SHOWSELALWAYS

Always show the selection, if any, even if the control does not have the focus.


### -field MMC_NOSORTHEADER

A value that specifies that column headers do not work like buttons. This style is useful if clicking a column header in report view does not carry out an action, such as sorting.


### -field MMC_ENSUREFOCUSVISIBLE



