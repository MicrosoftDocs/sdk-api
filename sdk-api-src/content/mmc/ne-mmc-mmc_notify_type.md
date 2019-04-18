---
UID: NE:mmc._MMC_NOTIFY_TYPE
title: MMC_NOTIFY_TYPE (mmc.h)
author: windows-sdk-content
description: The MMC_NOTIFY_TYPE enumeration defines the notifications of user actions that can be sent to a snap-in by the console's Node Manager when it calls IComponentData::Notify, IComponent::Notify, or IExtendControlbar::ControlbarNotify.
old-location: mmc\mmc_notify_type.htm
tech.root: mmc
ms.assetid: 3eeea87f-a29f-4e20-8906-e3cbdce00d57
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MMCN_ACTIVATE, MMCN_ADD_IMAGES, MMCN_BTN_CLICK, MMCN_CANPASTE_OUTOFPROC, MMCN_CLICK, MMCN_COLUMNS_CHANGED, MMCN_COLUMN_CLICK, MMCN_CONTEXTHELP, MMCN_CONTEXTMENU, MMCN_CUTORMOVE, MMCN_DBLCLICK, MMCN_DELETE, MMCN_DESELECT_ALL, MMCN_EXPAND, MMCN_EXPANDSYNC, MMCN_FILTERBTN_CLICK, MMCN_FILTER_CHANGE, MMCN_HELP, MMCN_INITOCX, MMCN_LISTPAD, MMCN_MENU_BTNCLICK, MMCN_MINIMIZED, MMCN_PASTE, MMCN_PRELOAD, MMCN_PRINT, MMCN_PROPERTY_CHANGE, MMCN_QUERY_PASTE, MMCN_REFRESH, MMCN_REMOVE_CHILDREN, MMCN_RENAME, MMCN_RESTORE_VIEW, MMCN_SELECT, MMCN_SHOW, MMCN_SNAPINHELP, MMCN_VIEW_CHANGE, MMC_NOTIFY_TYPE, MMC_NOTIFY_TYPE enumeration [MMC], _slate_mmc_notify_type, mmc.mmc_notify_type, mmc/MMCN_ACTIVATE, mmc/MMCN_ADD_IMAGES, mmc/MMCN_BTN_CLICK, mmc/MMCN_CANPASTE_OUTOFPROC, mmc/MMCN_CLICK, mmc/MMCN_COLUMNS_CHANGED, mmc/MMCN_COLUMN_CLICK, mmc/MMCN_CONTEXTHELP, mmc/MMCN_CONTEXTMENU, mmc/MMCN_CUTORMOVE, mmc/MMCN_DBLCLICK, mmc/MMCN_DELETE, mmc/MMCN_DESELECT_ALL, mmc/MMCN_EXPAND, mmc/MMCN_EXPANDSYNC, mmc/MMCN_FILTERBTN_CLICK, mmc/MMCN_FILTER_CHANGE, mmc/MMCN_HELP, mmc/MMCN_INITOCX, mmc/MMCN_LISTPAD, mmc/MMCN_MENU_BTNCLICK, mmc/MMCN_MINIMIZED, mmc/MMCN_PASTE, mmc/MMCN_PRELOAD, mmc/MMCN_PRINT, mmc/MMCN_PROPERTY_CHANGE, mmc/MMCN_QUERY_PASTE, mmc/MMCN_REFRESH, mmc/MMCN_REMOVE_CHILDREN, mmc/MMCN_RENAME, mmc/MMCN_RESTORE_VIEW, mmc/MMCN_SELECT, mmc/MMCN_SHOW, mmc/MMCN_SNAPINHELP, mmc/MMCN_VIEW_CHANGE, mmc/MMC_NOTIFY_TYPE
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
 - MMC_NOTIFY_TYPE
product: Windows
targetos: Windows
req.typenames: MMC_NOTIFY_TYPE
req.redist: 
ms.custom: 19H1
---

# MMC_NOTIFY_TYPE enumeration


## -description


The 
MMC_NOTIFY_TYPE enumeration defines the notifications of user actions that can be sent to a snap-in by the console's Node Manager when it calls 
<a href="https://msdn.microsoft.com/8679396e-23d0-4418-987a-c72b1508e7b9">IComponentData::Notify</a>, 
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a>, or 
<a href="https://msdn.microsoft.com/124656df-5d12-4de1-9a71-ba080ef36611">IExtendControlbar::ControlbarNotify</a>. For more information, see <a href="https://msdn.microsoft.com/8d5aa622-5668-495a-bc3a-25b863fbcb81">MMC Notifications</a>.


## -enum-fields




### -field MMCN_ACTIVATE

A window for which the snap-in owns the result view is being activated or deactivated.


### -field MMCN_ADD_IMAGES

The snap-in is being notified to add images for the result pane.


### -field MMCN_BTN_CLICK

The user clicked a toolbar button.


### -field MMCN_CLICK

Not used.


### -field MMCN_COLUMN_CLICK

The user clicked a list view column header.


### -field MMCN_CONTEXTMENU

Not used.


### -field MMCN_CUTORMOVE

Items owned by the snap-in have been cut or moved.


### -field MMCN_DBLCLICK

The user double-clicked a mouse button on a list view item or on a scope item in the result pane.


### -field MMCN_DELETE

Sent to 
     inform the snap-in that an object should be deleted.


### -field MMCN_DESELECT_ALL

Sent to the virtual list view when all items of an owner-data result pane are deselected.


### -field MMCN_EXPAND

Sent when a scope item must be expanded or collapsed.


### -field MMCN_HELP

Not used.


### -field MMCN_MENU_BTNCLICK

Sent when the user clicks a snap-in defined menu button.


### -field MMCN_MINIMIZED

Sent when a window is being minimized or maximized.


### -field MMCN_PASTE

Notifies the snap-in's scope item to paste selected result items.


### -field MMCN_PROPERTY_CHANGE

Informs the snap-in of property changes.


### -field MMCN_QUERY_PASTE

Sent to determine whether the snap-in can paste  items from a given data object.


### -field MMCN_REFRESH

Sent when the refresh verb is selected.


### -field MMCN_REMOVE_CHILDREN

Notifies the snap-in when to delete all the child items (the entire subtree) below a specified item.


### -field MMCN_RENAME

A scope or result item must be renamed.


### -field MMCN_SELECT

An item has been selected in either the scope pane or result pane.


### -field MMCN_SHOW

Sent when a scope item is selected or deselected.


### -field MMCN_VIEW_CHANGE

Sent to inform  the snap-in that the view should be updated.


### -field MMCN_SNAPINHELP

The user requested help about the snap-in.


### -field MMCN_CONTEXTHELP

The user requested help about a selected item.


### -field MMCN_INITOCX

Sent when a custom OCX is initialized for the first time.


### -field MMCN_FILTER_CHANGE

Sent when the filter value for a filtered result view column has been changed.


### -field MMCN_FILTERBTN_CLICK

The user clicked the filter button on the header control of a filtered view.


### -field MMCN_RESTORE_VIEW

Sent when the result pane for a scope item must be restored.


### -field MMCN_PRINT

Sent when the user clicks the <b>Print</b> button or selects the <b>Print</b> menu item.


### -field MMCN_PRELOAD

Sent if the snap-in supports the CCF_SNAPIN_PRELOADS format.


### -field MMCN_LISTPAD

Sent when the list control for the list view taskpad is being attached or detached.


### -field MMCN_EXPANDSYNC

Sent when MMC requires a scope item to be expanded synchronously.


### -field MMCN_COLUMNS_CHANGED

Sent when the user hides columns or makes columns visible in the list view.


### -field MMCN_CANPASTE_OUTOFPROC

Sent by MMC to determine whether the snap-in supports paste operations from another MMC process.


## -see-also




<a href="https://msdn.microsoft.com/8d5aa622-5668-495a-bc3a-25b863fbcb81">MMC Notifications</a>
 

 

