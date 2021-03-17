---
UID: NF:mmc.IExtendContextMenu.Command
title: IExtendContextMenu::Command (mmc.h)
description: The IExtendContextMenu::Command method is called if one of the items you added to the context menu with IExtendContextMenu::AddMenuItems is subsequently selected.
helpviewer_keywords: ["Command","Command method [MMC]","Command method [MMC]","IExtendContextMenu interface","IExtendContextMenu interface [MMC]","Command method","IExtendContextMenu.Command","IExtendContextMenu::Command","_slate_iextendcontextmenu_command","mmc.iextendcontextmenu_command","mmc/IExtendContextMenu::Command"]
old-location: mmc\iextendcontextmenu_command.htm
tech.root: mmc
ms.assetid: ee91a737-c6b4-48a1-88a2-57bef3730f5e
ms.date: 12/05/2018
ms.keywords: Command, Command method [MMC], Command method [MMC],IExtendContextMenu interface, IExtendContextMenu interface [MMC],Command method, IExtendContextMenu.Command, IExtendContextMenu::Command, _slate_iextendcontextmenu_command, mmc.iextendcontextmenu_command, mmc/IExtendContextMenu::Command
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
 - IExtendContextMenu::Command
 - mmc/IExtendContextMenu::Command
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
 - IExtendContextMenu.Command
---

# IExtendContextMenu::Command


## -description

The <b>IExtendContextMenu::Command</b> method is called if one of the items you added to the context menu with 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems">IExtendContextMenu::AddMenuItems</a> is subsequently selected. MMC calls 
Command with the command ID you specified and another pointer to the same 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface.

## -parameters

### -param lCommandID [in]

A value that specifies the command identifier of the menu item.

### -param piDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object whose context menu was displayed.

## -returns

This method can return one of these values.

## -remarks

MMC reserves negative-valued command IDs for predefined menu command IDs that it sends to a snap-in's IExtendContextMenu::Command method. The –1 command ID is the MMCC_STANDARD_VIEW_SELECT enumerator value defined in mmc.h. This is sent to IExtendContextMenu::Command when the user clicks a standard view command on the 
<b>View</b> menu (Large, Small, List, or Detail). This notifies the snap-in that the user is switching away from a custom view (OCX, HTML). After getting an MMCC_STANDARD_VIEW_SELECT command, the snap-in should request a standard view the next time its 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> method is called and not request a custom view until one of its custom view menu items is selected. If the snap-in only uses standard views or only uses custom views, it can ignore the MMCC_STANDARD_VIEW_SELECT command.

MMC sends the snap-in the MMCC_STANDARD_VIEW_SELECT command when the user clicks the 
<b>Back</b> button on the toolbar. MMC uses this command to instruct the snap-in to display the result pane's previous view.

## -see-also

<a href="/windows/desktop/api/mmc/ns-mmc-contextmenuitem">CONTEXTMENUITEM</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>



<a href="/previous-versions/windows/desktop/mmc/working-with-context-menus">Working with Context Menus</a>