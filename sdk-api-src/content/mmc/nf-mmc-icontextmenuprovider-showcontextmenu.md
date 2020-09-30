---
UID: NF:mmc.IContextMenuProvider.ShowContextMenu
title: IContextMenuProvider::ShowContextMenu (mmc.h)
description: The IContextMenuProvider::ShowContextMenu method displays a context menu.
helpviewer_keywords: ["IContextMenuProvider interface [MMC]","ShowContextMenu method","IContextMenuProvider.ShowContextMenu","IContextMenuProvider::ShowContextMenu","ShowContextMenu","ShowContextMenu method [MMC]","ShowContextMenu method [MMC]","IContextMenuProvider interface","_slate_icontextmenuprovider_showcontextmenu","mmc.icontextmenuprovider_showcontextmenu","mmc/IContextMenuProvider::ShowContextMenu"]
old-location: mmc\icontextmenuprovider_showcontextmenu.htm
tech.root: mmc
ms.assetid: 8fe9f474-c47b-4b53-8cbc-d658c82d7591
ms.date: 12/05/2018
ms.keywords: IContextMenuProvider interface [MMC],ShowContextMenu method, IContextMenuProvider.ShowContextMenu, IContextMenuProvider::ShowContextMenu, ShowContextMenu, ShowContextMenu method [MMC], ShowContextMenu method [MMC],IContextMenuProvider interface, _slate_icontextmenuprovider_showcontextmenu, mmc.icontextmenuprovider_showcontextmenu, mmc/IContextMenuProvider::ShowContextMenu
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
 - IContextMenuProvider::ShowContextMenu
 - mmc/IContextMenuProvider::ShowContextMenu
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
 - IContextMenuProvider.ShowContextMenu
---

# IContextMenuProvider::ShowContextMenu


## -description

The <b>IContextMenuProvider::ShowContextMenu</b> method displays a context menu.

## -parameters

### -param hwndParent [in]

A handle to the parent window in which the context menu is displayed.

### -param xPos [in]

A value, in screen coordinates, that specifies the horizontal location of the upper-left corner of the context menu, in screen coordinates.

### -param yPos [in]

A value, in screen coordinates, that specifies the vertical location of the upper-left corner of the context menu.

### -param plSelected [out]

A value that specifies the ICommandID value (as passed to 
<a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback-additem">IContextMenuCallback::AddItem</a>) of the selected menu item. If this is zero, either none of the context menu items were selected or the selected context menu item was added by an extension. If an extension item was selected, 
ShowContextMenu notifies the extension by calling 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-command">IExtendContextMenu::Command</a>.

## -returns

This method can return one of these values.

## -remarks

ShowContextMenu automatically clears the context menu after that displays it. A best practice is to call 
<a href="/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-emptymenulist">IContextMenuProvider::EmptyMenuList</a> before beginning to build a context menu.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>