---
UID: NS:mmc._MMC_RESTORE_VIEW
title: MMC_RESTORE_VIEW (mmc.h)
description: The MMC_RESTORE_VIEW structure is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_RESTORE_VIEW","MMC_RESTORE_VIEW structure [MMC]","_slate_mmc_restore_view","mmc.mmc_restore_view","mmc/MMC_RESTORE_VIEW"]
old-location: mmc\mmc_restore_view.htm
tech.root: mmc
ms.assetid: 349357e5-5d60-491f-b267-b18a52b4c927
ms.date: 12/05/2018
ms.keywords: MMC_RESTORE_VIEW, MMC_RESTORE_VIEW structure [MMC], _slate_mmc_restore_view, mmc.mmc_restore_view, mmc/MMC_RESTORE_VIEW
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
targetos: Windows
req.typenames: MMC_RESTORE_VIEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_RESTORE_VIEW
 - mmc/_MMC_RESTORE_VIEW
 - MMC_RESTORE_VIEW
 - mmc/MMC_RESTORE_VIEW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_RESTORE_VIEW
---

# MMC_RESTORE_VIEW structure


## -description

The 
MMC_RESTORE_VIEW structure is introduced in MMC 1.1.

The 
MMC_RESTORE_VIEW structure contains information about a result pane view that must be restored by the snap-in when the user has navigated to a view displayed in the view history using the back or forward buttons.

## -struct-fields

### -field dwSize

A value that specifies the size of the 
MMC_RESTORE_VIEW structure. A snap-in can use dwSize to check the version of the structure.

### -field cookie

A value that specifies the cookie for the item that will be restored in the scope pane.

### -field pViewType

A pointer to a string that specifies the view type used to display the result pane for the item specified by cookie. For more information about view types, see the ppViewType parameter for 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>.

### -field lViewOptions

A value that specifies the view option settings used to display the result pane for the item specified by cookie. For more information about view options, see the pViewOptions parameter of <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>.

## -remarks

MMC maintains a navigational history of the result pane. For each item in the history, MMC stores the view type and view options specified by <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> when the result pane was originally displayed during the course of the current console session. When the back or forward buttons are used to navigate the history, MMC sends the snap-in that owns that item an 
<a href="/previous-versions/windows/desktop/mmc/mmcn-restore-view">MMCN_RESTORE_VIEW</a> notification that has a pointer to an 
MMC_RESTORE_VIEW structure as its arg parameter and a pointer to a BOOL as its param parameter. The snap-in should handle that notification by setting the appropriate menu item in the 
<b>View</b> context menu, setting its internal view type state, and performing any initialization necessary to display the result pane as it appeared at that point in the view history.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-restore-view">MMCN_RESTORE_VIEW</a>