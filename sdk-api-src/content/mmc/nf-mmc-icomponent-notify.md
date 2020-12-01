---
UID: NF:mmc.IComponent.Notify
title: IComponent::Notify (mmc.h)
description: The IComponent::Notify method notifies the snap-in of actions taken by the user.
helpviewer_keywords: ["IComponent interface [MMC]","Notify method","IComponent.Notify","IComponent::Notify","Notify","Notify method [MMC]","Notify method [MMC]","IComponent interface","_slate_icomponent_notify","mmc.icomponent_notify","mmc/IComponent::Notify"]
old-location: mmc\icomponent_notify.htm
tech.root: mmc
ms.assetid: 38c3b31f-356c-46cf-904a-98241c0f199f
ms.date: 12/05/2018
ms.keywords: IComponent interface [MMC],Notify method, IComponent.Notify, IComponent::Notify, Notify, Notify method [MMC], Notify method [MMC],IComponent interface, _slate_icomponent_notify, mmc.icomponent_notify, mmc/IComponent::Notify
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponent::Notify
 - mmc/IComponent::Notify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponent.Notify
---

# IComponent::Notify


## -description

The <b>IComponent::Notify</b> method notifies the snap-in of actions taken by the user.

## -parameters

### -param lpDataObject [in]

A pointer to the data object of the currently selected item.

### -param event [in]

Identifies an action taken by a user. <b>IComponent::Notify</b> can receive the following notifications:


<a href="/previous-versions/windows/desktop/mmc/mmcn-activate">MMCN_ACTIVATE</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-add-images">MMCN_ADD_IMAGES</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-btn-click">MMCN_BTN_CLICK</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-column-click">MMCN_COLUMN_CLICK</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-columns-changed">MMCN_COLUMNS_CHANGED</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-contexthelp">MMCN_CONTEXTHELP</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-dblclick">MMCN_DBLCLICK</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-delete">MMCN_DELETE</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-deselect-all">MMCN_DESELECT_ALL</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-filterbtn-click">MMCN_FILTERBTN_CLICK</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-filter-change">MMCN_FILTER_CHANGE</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-initocx">MMCN_INITOCX</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-listpad">MMCN_LISTPAD</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-minimized">MMCN_MINIMIZED</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-paste">MMCN_PASTE</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-print">MMCN_PRINT</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-query-paste">MMCN_QUERY_PASTE</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-refresh">MMCN_REFRESH</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-rename">MMCN_RENAME</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-restore-view">MMCN_RESTORE_VIEW</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-select">MMCN_SELECT</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-show">MMCN_SHOW</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-snapinhelp">MMCN_SNAPINHELP</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-view-change">MMCN_VIEW_CHANGE</a>

### -param arg

Depends on the notification type.

### -param param

Depends on the notification type.

## -returns

This method can return one of these values.

## -remarks

For more information, see the individual notifications. The snap-in should return <b>S_FALSE</b> for any notification it does not handle.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontrolbar-controlbarnotify">IExtendControlbar::ControlbarNotify</a>