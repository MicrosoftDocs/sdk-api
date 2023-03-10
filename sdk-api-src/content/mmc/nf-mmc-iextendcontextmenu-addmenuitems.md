---
UID: NF:mmc.IExtendContextMenu.AddMenuItems
title: IExtendContextMenu::AddMenuItems (mmc.h)
description: The IExtendContextMenu::AddMenuItems method enables a snap-in to add items to a context menu.
helpviewer_keywords: ["AddMenuItems","AddMenuItems method [MMC]","AddMenuItems method [MMC]","IExtendContextMenu interface","CCM_INSERTIONALLOWED_NEW","CCM_INSERTIONALLOWED_TASK","CCM_INSERTIONALLOWED_TOP","CCM_INSERTIONALLOWED_VIEW","IExtendContextMenu interface [MMC]","AddMenuItems method","IExtendContextMenu.AddMenuItems","IExtendContextMenu::AddMenuItems","_slate_iextendcontextmenu_addmenuitems","mmc.iextendcontextmenu_addmenuitems","mmc/IExtendContextMenu::AddMenuItems"]
old-location: mmc\iextendcontextmenu_addmenuitems.htm
tech.root: mmc
ms.assetid: d4fc7bfd-b017-466e-81f2-74f13aec4b52
ms.date: 12/05/2018
ms.keywords: AddMenuItems, AddMenuItems method [MMC], AddMenuItems method [MMC],IExtendContextMenu interface, CCM_INSERTIONALLOWED_NEW, CCM_INSERTIONALLOWED_TASK, CCM_INSERTIONALLOWED_TOP, CCM_INSERTIONALLOWED_VIEW, IExtendContextMenu interface [MMC],AddMenuItems method, IExtendContextMenu.AddMenuItems, IExtendContextMenu::AddMenuItems, _slate_iextendcontextmenu_addmenuitems, mmc.iextendcontextmenu_addmenuitems, mmc/IExtendContextMenu::AddMenuItems
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
 - IExtendContextMenu::AddMenuItems
 - mmc/IExtendContextMenu::AddMenuItems
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
 - IExtendContextMenu.AddMenuItems
---

# IExtendContextMenu::AddMenuItems


## -description

The <b>IExtendContextMenu::AddMenuItems</b> method enables a snap-in to add items to a context menu.

## -parameters

### -param piDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object of the menu to which items are added.

### -param piCallback [in]

A pointer to an 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a> that can add items to the context menu.

### -param pInsertionAllowed [in, out]

A value that identifies MMC-defined menu-item insertion points that can be used. This can be a combination of the following flags:



#### CCM_INSERTIONALLOWED_TOP

Items can be inserted at the top of a context menu.



#### CCM_INSERTIONALLOWED_NEW

Items can be inserted in the New submenu.



#### CCM_INSERTIONALLOWED_TASK

Items can be inserted in the All Tasks submenu.



#### CCM_INSERTIONALLOWED_VIEW

Items can be inserted in the toolbar view menu or in the 
<b>View</b> submenu of the result pane context menu.

## -returns

This method can return one of these values.

## -remarks

An implementation of <b>IExtendContextMenu::AddMenuItems</b> typically reads the node type and any other parameters required by calling 
IDataObject::GetDataHere on piDataObject, then adds context menu items as appropriate by calling 
<a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback-additem">IContextMenuCallback::AddItem</a> on piCallback.

Your snap-in should check the pInsertionsAllowed flags for permission before attempting to add menu items at the MMC-defined insertion points. For example, a snap-in should not add menu items to CCM_INSERTIONPOINTID_PRIMARY_NEW or CCM_INSERTIONPOINTID_3RDPARTY_NEW unless the CCM_INSERTIONALLOWED_NEW flag is set.

The pInsertionsAllowed flags allow the following two features:



If the user selects a scope item and then displays its context menu, MMC will give both the snap-in's 
IComponentData and 
IComponent (that owns the current view) implementations the opportunity to add menu items. MMC calls the IExtendContextMenu::AddMenuItems method implemented by the snap-in's 
IComponent implementation to allow the snap-in to add menu items to the 
<b>View</b> menu. MMC calls the IExtendContextMenu::AddMenuItems method implemented by the snap-in's 
IComponentData to allow the snap-in to add menu items to all other menus. Only the snap-in's 
IComponent implementation can add items to the 
<b>View</b> menu.

If the user displays a scope item's context menu without first selecting the scope item, MMC will only give the snap-in's 
IComponentData implementation the opportunity to add menu items to all menus except for the 
<b>View</b> menu. Consequently, the 
<b>View</b> menu only appears for a scope item if the user first selects an item.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The 
AddMenuItems method should not call AddRef on either the piDataObject pointer or the piCallback pointer, nor should it call the methods of those interfaces after returning. Instead, it should make all necessary calls to the methods of those interfaces before returning. If any of these items is selected, you will be given back the pointer to IDataObject in 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-command">IExtendContextMenu::Command</a>, so do not keep this pointer after this method returns. You will not be notified if the menu is dismissed without any of your items being selected. In addition, do not query for alternate interfaces from piCallback because the one method, IContextMenuCallback::AddItem, should be sufficient.

## -see-also

<a href="/windows/desktop/api/mmc/ns-mmc-contextmenuitem">CONTEXTMENUITEM</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>



<a href="/previous-versions/windows/desktop/mmc/working-with-context-menus">Working with Context Menus</a>