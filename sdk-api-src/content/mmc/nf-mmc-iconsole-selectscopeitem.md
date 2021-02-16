---
UID: NF:mmc.IConsole.SelectScopeItem
title: IConsole::SelectScopeItem (mmc.h)
description: Selects the given scope item.
helpviewer_keywords: ["IConsole interface [MMC]","SelectScopeItem method","IConsole.SelectScopeItem","IConsole::SelectScopeItem","SelectScopeItem","SelectScopeItem method [MMC]","SelectScopeItem method [MMC]","IConsole interface","mmc.iconsole_selectscopeitem","mmc/IConsole::SelectScopeItem"]
old-location: mmc\iconsole_selectscopeitem.htm
tech.root: mmc
ms.assetid: ADE56DDF-C437-4BF3-A2EC-1E35EE7567F3
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],SelectScopeItem method, IConsole.SelectScopeItem, IConsole::SelectScopeItem, SelectScopeItem, SelectScopeItem method [MMC], SelectScopeItem method [MMC],IConsole interface, mmc.iconsole_selectscopeitem, mmc/IConsole::SelectScopeItem
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
 - IConsole::SelectScopeItem
 - mmc/IConsole::SelectScopeItem
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
 - IConsole.SelectScopeItem
---

# IConsole::SelectScopeItem


## -description

Selects the given scope item.

## -parameters

### -param hScopeItem [in]

A handle to the item in the scope pane to be selected.

## -returns

This method can return one of these values.

## -remarks

Use this method to reselect the currently selected scope item or to select another scope item.

You can have a single scope item with several different views available, for example, several OLE custom control (OCX) views and the default list view. When the user selects a different view from a menu, the snap-in receives the command and should then call 
<b>SelectScopeItem</b> to reselect the item. 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> can then return the new view type.

If 
<b>SelectScopeItem</b> is called by the snap-in in its <a href="/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a> notification handler, MMC will not select the specified scope item, even though 
<b>SelectScopeItem</b> may return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>