---
UID: NS:mmc._CONTEXTMENUITEM
title: CONTEXTMENUITEM (mmc.h)
description: The CONTEXTMENUITEM structure is passed to the IContextMenuCallback::AddItem method or the IContextMenuProvider::AddItem method (inherited from IContextMenuCallback) to define a new menu item, submenu, or insertion point.
helpviewer_keywords: ["*LPCONTEXTMENUITEM","0 (zero)","CCM_COMMANDID_MASK_RESERVED = 0xFFFF0000","CCM_INSERTIONPOINTID_3RDPARTY_NEW = 0x90000001","CCM_INSERTIONPOINTID_3RDPARTY_TASK = 0x90000002","CCM_INSERTIONPOINTID_MASK_ADD_3RDPARTY = 0x10000000","CCM_INSERTIONPOINTID_MASK_ADD_PRIMARY = 0x20000000","CCM_INSERTIONPOINTID_MASK_CREATE_PRIMARY = 0x40000000","CCM_INSERTIONPOINTID_MASK_RESERVED = 0x0FFF0000","CCM_INSERTIONPOINTID_MASK_SHARED = 0x80000000","CCM_INSERTIONPOINTID_MASK_SPECIAL = 0xFFFF0000","CCM_INSERTIONPOINTID_PRIMARY_NEW = 0xA0000001","CCM_INSERTIONPOINTID_PRIMARY_TASK = 0xA0000002","CCM_INSERTIONPOINTID_PRIMARY_TOP = 0xA0000000","CCM_INSERTIONPOINTID_PRIMARY_VIEW = 0xA0000003","CCM_INSERTIONPOINTID_ROOT_MENU = 0x80000000","CCM_SPECIAL_DEFAULT_ITEM = 0x0004","CCM_SPECIAL_INSERTION_POINT = 0x0008","CCM_SPECIAL_SEPARATOR = 0x0001","CCM_SPECIAL_SUBMENU = 0x0002","CCM_SPECIAL_TESTONLY = 0x0010","CONTEXTMENUITEM","CONTEXTMENUITEM structure [MMC]","LPCONTEXTMENUITEM","LPCONTEXTMENUITEM structure pointer [MMC]","MF_BITMAP MF_OWNERDRAW","MF_CHECKED","MF_DISABLED","MF_ENABLED","MF_GRAYED","MF_MENUBARBREAK","MF_MENUBREAK","MF_POPUP","MF_SEPARATOR","MF_UNCHECKED","_slate_contextmenuitem","mmc.contextmenuitem","mmc/CONTEXTMENUITEM","mmc/LPCONTEXTMENUITEM"]
old-location: mmc\contextmenuitem.htm
tech.root: mmc
ms.assetid: 58a0b4cf-0379-48a1-80c6-5245022cf891
ms.date: 12/05/2018
ms.keywords: '*LPCONTEXTMENUITEM, 0 (zero), CCM_COMMANDID_MASK_RESERVED = 0xFFFF0000, CCM_INSERTIONPOINTID_3RDPARTY_NEW = 0x90000001, CCM_INSERTIONPOINTID_3RDPARTY_TASK = 0x90000002, CCM_INSERTIONPOINTID_MASK_ADD_3RDPARTY = 0x10000000, CCM_INSERTIONPOINTID_MASK_ADD_PRIMARY = 0x20000000, CCM_INSERTIONPOINTID_MASK_CREATE_PRIMARY = 0x40000000, CCM_INSERTIONPOINTID_MASK_RESERVED = 0x0FFF0000, CCM_INSERTIONPOINTID_MASK_SHARED = 0x80000000, CCM_INSERTIONPOINTID_MASK_SPECIAL = 0xFFFF0000, CCM_INSERTIONPOINTID_PRIMARY_NEW = 0xA0000001, CCM_INSERTIONPOINTID_PRIMARY_TASK = 0xA0000002, CCM_INSERTIONPOINTID_PRIMARY_TOP = 0xA0000000, CCM_INSERTIONPOINTID_PRIMARY_VIEW = 0xA0000003, CCM_INSERTIONPOINTID_ROOT_MENU = 0x80000000, CCM_SPECIAL_DEFAULT_ITEM = 0x0004, CCM_SPECIAL_INSERTION_POINT = 0x0008, CCM_SPECIAL_SEPARATOR = 0x0001, CCM_SPECIAL_SUBMENU = 0x0002, CCM_SPECIAL_TESTONLY = 0x0010, CONTEXTMENUITEM, CONTEXTMENUITEM structure [MMC], LPCONTEXTMENUITEM, LPCONTEXTMENUITEM structure pointer [MMC], MF_BITMAP MF_OWNERDRAW, MF_CHECKED, MF_DISABLED, MF_ENABLED, MF_GRAYED, MF_MENUBARBREAK, MF_MENUBREAK, MF_POPUP, MF_SEPARATOR, MF_UNCHECKED, _slate_contextmenuitem, mmc.contextmenuitem, mmc/CONTEXTMENUITEM, mmc/LPCONTEXTMENUITEM'
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
req.typenames: CONTEXTMENUITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CONTEXTMENUITEM
 - mmc/_CONTEXTMENUITEM
 - CONTEXTMENUITEM
 - mmc/CONTEXTMENUITEM
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
 - CONTEXTMENUITEM
---

# CONTEXTMENUITEM structure


## -description

The <b>CONTEXTMENUITEM</b> structure is passed to the 
    <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback-additem">IContextMenuCallback::AddItem</a> method or the 
    <b>IContextMenuProvider::AddItem</b> method 
    (inherited from <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>) to define a new 
    menu item, submenu, or insertion point. The context menu is built from the root down, with each new item going to 
    the end of the submenu or insertion point where it is inserted.

## -struct-fields

### -field strName

A pointer to a null-terminated string that contains the name of the menu item or of the submenu. This member cannot be <b>NULL</b> except for a separator or insertion point.

### -field strStatusBarText

A pointer to a null-terminated string that contains the text that is displayed in the status bar when this item is highlighted. This member can be <b>NULL</b>.

### -field lCommandID

A value that specifies the command identifier for menu items. If this menu item is added by 
       <a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems">IExtendContextMenu::AddMenuItems</a> and 
       then selected, this is the command ID that is passed back to 
       <a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-command">IExtendContextMenu::Command</a>. If this menu 
       item is added by the <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> 
       interface and then selected, this is the command ID that is passed back to pISelected by 
       <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-showcontextmenu">IContextMenuProvider::ShowContextMenu</a>. 
       If this is an insertion point (<b>CCM_SPECIAL_INSERTION_POINT</b> is set in 
       <i>fSpecialFlags</i>) or a submenu (<b>MF_POPUP</b> is set in 
       <i>fFlags</i>), use <i>lCommandID</i> in subsequent calls as 
       <i>lInsertionPointID</i> (for more information, see the following list). Carefully read the 
       following discussion because specific bits in the new insertion point ID must be on and others must be off.

Some bits in the command ID require special handling for items that are not insertion points or submenus.



#### CCM_COMMANDID_MASK_RESERVED = 0xFFFF0000

Items other than insertion points and submenus cannot be added when these bits are set.

Some bits in the insertion point ID require special handling for items that are insertion points (<i>fSpecialFlags</i> and <b>CCM_SPECIAL_INSERTION_POINT</b>) or submenus (<i>fFlags</i> and <b>MF_POPUP</b>).



#### CCM_INSERTIONPOINTID_MASK_SPECIAL = 0xFFFF0000

Special behavior. Snap-ins can use the other bits as required.



#### CCM_INSERTIONPOINTID_MASK_SHARED = 0x80000000

These insertion points and submenus are shared between the creator of the context menu, the primary extension, and the third-party extension. Items added to a shared insertion point or submenu are available to the creator of the context menu, the primary extension, and the third-party extension.

If this bit is not set, the 
         <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> interface and each extension can use the same ID. Each ID refers to a different insertion point or submenu.

Only the context menu creator and the primary snap-in can create shared insertion points or submenus.



#### CCM_INSERTIONPOINTID_MASK_CREATE_PRIMARY = 0x40000000

This bit must be set for shared insertion points and submenus created by the primary snap-in and not set for those created by the context menu creator. This prevents ID conflicts between the two sources of shared insertion points and submenus.



#### CCM_INSERTIONPOINTID_MASK_ADD_PRIMARY = 0x20000000

Allow the primary snap-in to add items to a shared insertion point or submenu.



#### CCM_INSERTIONPOINTID_MASK_ADD_3RDPARTY = 0x10000000

Allow extension snap-ins to add items to a shared insertion point or submenu.



#### CCM_INSERTIONPOINTID_MASK_RESERVED = 0x0FFF0000

Insertion points or submenus cannot be added with any of these bits set.

### -field lInsertionPointID

A value that specifies where in the context menu the new item should be added. Snap-ins can only add items to insertion points created by the menu creator or the primary snap-in. The following are the insertion points created by MMC in the default context menus for items in the scope pane and list view result pane:



#### 0 (zero)

An <i>lInsertionPointID</i> of zero refers to the root menu for this context menu. Zero can be used interchangeably with <b>CCM_INSERTIONPOINTID_ROOT_MENU</b>. Be aware that only the 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> interface can add items directly to the root menu. Extensions can only add items to insertion points and submenus added to the root menu by 
<b>IContextMenuProvider</b> or by MMC.



#### CCM_INSERTIONPOINTID_PRIMARY_TOP = 0xA0000000

The primary snap-in can use this insertion point to add items to the top of the main context menu.



#### CCM_INSERTIONPOINTID_PRIMARY_NEW = 0xA0000001

The primary snap-in can use this insertion point to add items to the top of the New submenu. The New submenu is available in context menus in both the scope pane and the result pane.



#### CCM_INSERTIONPOINTID_PRIMARY_TASK = 0xA0000002

The primary snap-in can use this insertion point to add items to the top of the All Tasks submenu. The All Tasks submenu is available in context menus in both the scope pane and the result pane.



#### CCM_INSERTIONPOINTID_PRIMARY_VIEW = 0xA0000003

The primary snap-in can use this insertion point to add items to the 
<b>View</b> drop-down menu. If the user clicks the 
<b>View</b>  menu in the toolbar, this insertion point will be present, but the New and All Tasks insertion points will not appear.



#### CCM_INSERTIONPOINTID_3RDPARTY_NEW = 0x90000001

Extension snap-ins can use this insertion point to add items to the bottom of the New submenu. The New submenu is only present for context menus in the scope pane and not for context menus in the result pane.



#### CCM_INSERTIONPOINTID_3RDPARTY_TASK = 0x90000002

Extension snap-ins can use this insertion point to add items to the bottom of the All Tasks submenu.



#### CCM_INSERTIONPOINTID_ROOT_MENU = 0x80000000

The 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> interface can use this insertion point to add items to the root menu.

Neither primary extensions nor third-party extensions can add items to the root menu except through insertion points added by 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>.

### -field fFlags

A value that specifies one or more of the following style flags:



#### MF_POPUP

A value that specifies that this is a submenu within the context menu. Menu items, insertion points, and further submenus can be added to this submenu using its <i>lCommandID</i> as their <i>lInsertionPointID</i>.



#### MF_BITMAP
MF_OWNERDRAW

These flags are not supported and will result in 
<a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback-additem">IContextMenuCallback::AddItem</a> returning <b>E_INVALIDARG</b>.



#### MF_SEPARATOR

Draws a horizontal separator line.

Only the 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> interface can add menu items with <b>MF_SEPARATOR</b> set.

The following flags function in the same way that they do in the Windows API:



#### MF_CHECKED

Selects the menu item.



#### MF_DISABLED

Disables the menu item so it cannot be selected, but the flag does not gray it.



#### MF_ENABLED

Enables the menu item so it can be selected, restoring it from a grayed state.



#### MF_GRAYED

Disables the menu item, graying it so it cannot be selected.



#### MF_MENUBARBREAK

Functions the same as the <b>MF_MENUBREAK</b> flag for a menu bar. For a drop-down menu, submenu, or shortcut menu, the new column is separated from the old column by a vertical line.



#### MF_MENUBREAK

Places the item on a new line (for a menu bar) or in a new column (for a drop-down menu, submenu, or shortcut menu) without separating columns.



#### MF_UNCHECKED

Does not select the item (default).

The following groups of flags cannot be used together:

<ul>
<li><b>MF_DISABLED</b>, <b>MF_ENABLED</b>, and <b>MF_GRAYED</b></li>
<li><b>MF_MENUBARBREAK</b> and <b>MF_MENUBREAK</b></li>
<li><b>MF_CHECKED</b> and <b>MF_UNCHECKED</b></li>
</ul>

### -field fSpecialFlags

A value that specifies one or more of the following flags:



#### CCM_SPECIAL_SEPARATOR = 0x0001

Ignore all other parameters except <i>lInsertionPointID</i>. Add a separator to the end of the menu or at the specified insertion point. Separators placed at the top or bottom of a menu or submenu will not be displayed. Separators with no menu items between them will be collapsed into a single separator.

Only the 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> interface can add separators, special or otherwise.



#### CCM_SPECIAL_SUBMENU = 0x0002

If this submenu is empty, it will be grayed and disabled. This is only valid for <b>MF_POPUP</b> items.



#### CCM_SPECIAL_DEFAULT_ITEM = 0x0004

The default menu item. If more than one menu item specifies this flag, the last item in each submenu takes precedence.



#### CCM_SPECIAL_INSERTION_POINT = 0x0008

Ignore all other parameters except <i>lCommandID</i> and <i>lInsertionPointID</i>. This creates a new insertion point at the end of the insertion point or submenu identified by <i>lInsertionPointID</i>.

Subsequent calls can use the <i>lCommandID</i> parameter from this call as their <i>lInsertionPointID</i>, and insert their own menu items, submenus, or insertion points at this point in the menu.



#### CCM_SPECIAL_TESTONLY = 0x0010

Validate the item parameters, but do not add the menu item. Return result code that indicates whether add would have been successful.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>



<a href="/previous-versions/windows/desktop/mmc/working-with-context-menus">Working with Context Menus</a>