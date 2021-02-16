---
UID: NS:mmc._CONTEXTMENUITEM2
title: CONTEXTMENUITEM2 (mmc.h)
description: The CONTEXTMENUITEM2 structure is introduced in MMC 2.0.
helpviewer_keywords: ["*LPCONTEXTMENUITEM2","0 (zero)","CCM_COMMANDID_MASK_RESERVED","CCM_INSERTIONPOINTID_3RDPARTY_NEW","CCM_INSERTIONPOINTID_3RDPARTY_TASK","CCM_INSERTIONPOINTID_MASK_ADD_3RDPARTY","CCM_INSERTIONPOINTID_MASK_ADD_PRIMARY","CCM_INSERTIONPOINTID_MASK_CREATE_PRIMARY","CCM_INSERTIONPOINTID_MASK_RESERVED","CCM_INSERTIONPOINTID_MASK_SHARED","CCM_INSERTIONPOINTID_MASK_SPECIAL","CCM_INSERTIONPOINTID_PRIMARY_NEW","CCM_INSERTIONPOINTID_PRIMARY_TASK","CCM_INSERTIONPOINTID_PRIMARY_TOP","CCM_INSERTIONPOINTID_PRIMARY_VIEW","CCM_INSERTIONPOINTID_ROOT_MENU","CCM_SPECIAL_DEFAULT_ITEM","CCM_SPECIAL_INSERTION_POINT","CCM_SPECIAL_SEPARATOR","CCM_SPECIAL_SUBMENU","CCM_SPECIAL_TESTONLY = 0x0010","CONTEXTMENUITEM2","CONTEXTMENUITEM2 structure [MMC]","LPCONTEXTMENUITEM2","LPCONTEXTMENUITEM2 structure pointer [MMC]","MF_BITMAP","MF_CHECKED","MF_DISABLED","MF_ENABLED","MF_GRAYED","MF_MENUBARBREAK","MF_MENUBREAK","MF_OWNERDRAW","MF_POPUP","MF_SEPARATOR","MF_UNCHECKED","_slate_contextmenuitem2","mmc.contextmenuitem2","mmc/CONTEXTMENUITEM2","mmc/LPCONTEXTMENUITEM2"]
old-location: mmc\contextmenuitem2.htm
tech.root: mmc
ms.assetid: 5ed4429c-e147-4097-8d52-11f5319dce2a
ms.date: 12/05/2018
ms.keywords: '*LPCONTEXTMENUITEM2, 0 (zero), CCM_COMMANDID_MASK_RESERVED, CCM_INSERTIONPOINTID_3RDPARTY_NEW, CCM_INSERTIONPOINTID_3RDPARTY_TASK, CCM_INSERTIONPOINTID_MASK_ADD_3RDPARTY, CCM_INSERTIONPOINTID_MASK_ADD_PRIMARY, CCM_INSERTIONPOINTID_MASK_CREATE_PRIMARY, CCM_INSERTIONPOINTID_MASK_RESERVED, CCM_INSERTIONPOINTID_MASK_SHARED, CCM_INSERTIONPOINTID_MASK_SPECIAL, CCM_INSERTIONPOINTID_PRIMARY_NEW, CCM_INSERTIONPOINTID_PRIMARY_TASK, CCM_INSERTIONPOINTID_PRIMARY_TOP, CCM_INSERTIONPOINTID_PRIMARY_VIEW, CCM_INSERTIONPOINTID_ROOT_MENU, CCM_SPECIAL_DEFAULT_ITEM, CCM_SPECIAL_INSERTION_POINT, CCM_SPECIAL_SEPARATOR, CCM_SPECIAL_SUBMENU, CCM_SPECIAL_TESTONLY = 0x0010, CONTEXTMENUITEM2, CONTEXTMENUITEM2 structure [MMC], LPCONTEXTMENUITEM2, LPCONTEXTMENUITEM2 structure pointer [MMC], MF_BITMAP, MF_CHECKED, MF_DISABLED, MF_ENABLED, MF_GRAYED, MF_MENUBARBREAK, MF_MENUBREAK, MF_OWNERDRAW, MF_POPUP, MF_SEPARATOR, MF_UNCHECKED, _slate_contextmenuitem2, mmc.contextmenuitem2, mmc/CONTEXTMENUITEM2, mmc/LPCONTEXTMENUITEM2'
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
req.typenames: CONTEXTMENUITEM2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CONTEXTMENUITEM2
 - mmc/_CONTEXTMENUITEM2
 - CONTEXTMENUITEM2
 - mmc/CONTEXTMENUITEM2
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
 - CONTEXTMENUITEM2
---

# CONTEXTMENUITEM2 structure


## -description

The <b>CONTEXTMENUITEM2</b> structure is introduced in MMC 
    2.0.

The <b>CONTEXTMENUITEM2</b> structure is passed to the 
    <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback2-additem">IContextMenuCallback2::AddItem</a> method or 
    the <a href="/previous-versions/windows/desktop/legacy/aa814824(v=vs.85)">IContextMenuProvider::AddItem</a> method 
    (inherited from <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>) to define a new 
    menu item, submenu, or insertion point. The context menu is built from the root down, with each new item going to 
    the end of the submenu or insertion point where the new item is inserted. The 
    <b>CONTEXTMENUITEM2</b> structure supersedes the 
    <a href="/windows/desktop/api/mmc/ns-mmc-contextmenuitem">CONTEXTMENUITEM</a> structure (other than 
    the <b>strLanguageIndependentName</b> member, all of the members of 
    <b>CONTEXTMENUITEM2</b> are in 
    <b>CONTEXTMENUITEM</b>).

## -struct-fields

### -field strName

A pointer to a null-terminated string that contains the name of the menu item or of the submenu. This 
      member cannot be <b>NULL</b> except for a separator or insertion point.

### -field strStatusBarText

A pointer to a null-terminated string that contains the text that is displayed on the status bar when this 
      item is highlighted. This member can be <b>NULL</b>.

### -field lCommandID

A value that specifies the command identifier for menu items. If the menu item is added by 
       <a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems">IExtendContextMenu::AddMenuItems</a> and 
       then selected, <i>lCommandID</i> is the command ID parameter that is passed back to 
       <a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-command">IExtendContextMenu::Command</a>. If this menu 
       item is added by the <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> 
       interface and then selected, this is the command ID that is passed back to 
       <i>pISelected</i> by 
       <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenuprovider-showcontextmenu">IContextMenuProvider::ShowContextMenu</a>. 
       If this is an insertion point (<b>CCM_SPECIAL_INSERTION_POINT</b> is set in 
       <i>fSpecialFlags</i>) or a submenu (<i>MF_POPUP</i> is set in 
       <i>fFlags</i>), use <i>lCommandID</i> in subsequent calls as 
       <i>lInsertionPointID</i> (for more information, see the following list). Carefully read the 
       following discussion because specific bits in the new insertion point ID must be on and others must be off.

The following bits in the command ID require special handling for items that are not insertion points or 
       submenus.



#### CCM_COMMANDID_MASK_RESERVED (0xFFFF0000)

Items other than insertion points and submenus cannot be added when these bits are set.

The following bits in the insertion point ID require special handling for items that are insertion points 
       (<i>fSpecialFlags</i> and <b>CCM_SPECIAL_INSERTION_POINT</b>) or 
       submenus (<i>fFlags</i> and <b>MF_POPUP</b>).



#### CCM_INSERTIONPOINTID_MASK_SPECIAL (0xFFFF0000)

Special behavior. Snap-ins can use the other bits as required.



#### CCM_INSERTIONPOINTID_MASK_SHARED (0x80000000)

These insertion points and submenus are shared between the creator of the context menu, the primary 
         extension, and the third-party extension. Items added to a shared insertion point or submenu are available 
         to the creator of the context menu, the primary extension, and the third-party extension.

If this bit is not set, the 
         <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> interface and each 
         extension can use the same ID. Each ID refers to a different insertion point or submenu.

Only the context menu creator and the primary snap-in can create shared insertion points or submenus.



#### CCM_INSERTIONPOINTID_MASK_CREATE_PRIMARY (0x40000000)

This bit must be set for shared insertion points and submenus created by the primary snap-in and not set 
        for those created by the context menu creator. This prevents ID conflicts between the two sources of shared 
        insertion points and submenus.



#### CCM_INSERTIONPOINTID_MASK_ADD_PRIMARY (0x20000000)

Allows the primary snap-in to add items to a shared insertion point or submenu.



#### CCM_INSERTIONPOINTID_MASK_ADD_3RDPARTY (0x10000000)

Allows extension snap-ins to add items to a shared insertion point or submenu.



#### CCM_INSERTIONPOINTID_MASK_RESERVED (0x0FFF0000)

Insertion points or submenus cannot be added with this value set.

### -field lInsertionPointID

A value that specifies where in the context menu the new item should be added. Snap-ins can only add items 
      to insertion points that are created by the menu creator or the primary snap-in. The following are the 
      insertion points created by MMC in the default context menus for items in the scope pane and list view result 
      pane:



#### 0 (zero)

An <i>lInsertionPointID</i> of 0 refers to the root menu for this context menu. The 
        value 0 can be used interchangeably with <b>CCM_INSERTIONPOINTID_ROOT_MENU</b>. Be aware 
        that only <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> is permitted to 
        add items directly to the root menu. Extensions can only add items to insertion points and submenus added to 
        the root menu by <b>IContextMenuProvider</b> or by MMC.



#### CCM_INSERTIONPOINTID_PRIMARY_TOP (0xA0000000)

The primary snap-in can use this insertion point to add items to the top of the main context menu.



#### CCM_INSERTIONPOINTID_PRIMARY_NEW (0xA0000001)

The primary snap-in can use this insertion point to add items to the top of the 
        <b>New</b> submenu. The <b>New</b> submenu is available in context 
        menus of the scope and result panes.



#### CCM_INSERTIONPOINTID_PRIMARY_TASK (0xA0000002)

The primary snap-in can use this insertion point to add items to the top of the All Tasks submenu. The 
        <b>All Tasks</b> submenu is available in context menus of the scope and result 
        panes.



#### CCM_INSERTIONPOINTID_PRIMARY_VIEW (0xA0000003)

The primary snap-in can use this insertion point to add items to the <b>View</b> 
        menu. If the user clicks the <b>View</b> drop-down menu on the toolbar, this insertion 
        point will be present, but the New and All Tasks insertion points will not appear.



#### CCM_INSERTIONPOINTID_3RDPARTY_NEW (0x90000001)

Extension snap-ins can use this insertion point to add items to the bottom of the 
        <b>New</b> submenu. The <b>New</b> submenu is only present for 
        context menus in the scope pane and not for context menus in the result pane.



#### CCM_INSERTIONPOINTID_3RDPARTY_TASK (0x90000002)

Extension snap-ins can use this insertion point to add items to the bottom of the 
        <b>All Tasks</b> submenu.



#### CCM_INSERTIONPOINTID_ROOT_MENU (0x80000000)


<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> can use this insertion 
         point to add items to the root menu.

Neither primary extensions nor third-party extensions can add items to the root menu except through 
         insertion points added by <i>IContextMenuProvider</i>.

### -field fFlags

A value that specifies one or more of the following style flags:



#### MF_POPUP

The created item is a submenu within the context menu. Menu items, insertion points, and other submenus 
        can be added to the created submenu; the new menu item, submenu, or insertion point should use the created 
        submenu's <b>lCommandID</b> member as the <b>lInsertionPointID</b> 
        member value.



#### MF_BITMAP

This flags is not supported; 
        <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback2-additem">IContextMenuCallback2::AddItem</a> will 
        return <b>E_INVALIDARG</b>.



#### MF_OWNERDRAW

This flags is not supported; 
        <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback2-additem">IContextMenuCallback2::AddItem</a> will 
        return <b>E_INVALIDARG</b>.



#### MF_SEPARATOR

Draws a horizontal separator line.

Only <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> can add menu items 
         with <b>MF_SEPARATOR</b> set.

The following flags function in the same way as they do in the Windows API.



#### MF_CHECKED

Selects the menu item.



#### MF_DISABLED

Disables the menu item so that it cannot be selected, but the flag does not dim the menu item.



#### MF_ENABLED

Enables the menu item so that it can be selected, restoring it from its dimmed state.



#### MF_GRAYED

Disables the menu item, dimming it so that it cannot be selected.



#### MF_MENUBARBREAK

Functions the same as the <b>MF_MENUBREAK</b> flag for a menu bar. For a drop-down 
        menu, submenu, or shortcut menu, a vertical line separates the new column from the old column.



#### MF_MENUBREAK

Places the item on a new line (for a menu bar) or in a new column (for a drop-down menu, submenu, or 
        shortcut menu) without separating columns.



#### MF_UNCHECKED

Does not select the item (default).

The following groups of flags cannot be used together:

<ul>
<li><b>MF_DISABLED</b>, <b>MF_ENABLED</b>, and 
        <b>MF_GRAYED</b></li>
<li><b>MF_MENUBARBREAK</b> and <b>MF_MENUBREAK</b></li>
<li><b>MF_CHECKED</b> and <b>MF_UNCHECKED</b></li>
</ul>

### -field fSpecialFlags

A value that specifies one or more of the following flags:



#### CCM_SPECIAL_SEPARATOR (0x0001)

Ignore all other parameters except <i>lInsertionPointID</i>. Add a separator to the end 
         of the menu or at the specified insertion point. Separators placed at the top or bottom of a menu or submenu 
         will not be displayed. Separators with no menu items between them will be collapsed into a single 
         separator.

Only <a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a> can add separators, 
         special or otherwise.



#### CCM_SPECIAL_SUBMENU (0x0002)

If this submenu is empty, it appears dimmed; this is only valid for <b>MF_POPUP</b> 
        items.



#### CCM_SPECIAL_DEFAULT_ITEM (0x0004)

This is the default menu item. If more than one menu item specifies this flag, the last item in each 
        submenu takes precedence.



#### CCM_SPECIAL_INSERTION_POINT (0x0008)

Ignore all other parameters except <i>lCommandID</i> and 
        <i>lInsertionPointID</i>. This flag creates a new insertion point at the end of the 
        insertion point or submenu identified by <b>lInsertionPointID</b>. New menu items, 
        submenus, or insertion points can be added to the created insertion point; the new menu item, submenu, or 
        insertion point should use the created insertion point's <b>lCommandID</b> member as the 
        <b>lInsertionPointID</b> member value.



#### CCM_SPECIAL_TESTONLY = 0x0010

Validate the item parameters, but do not add the menu item. Returns a result code that indicates whether 
        an Add operation would have been successful.

### -field strLanguageIndependentName

The language-independent name of the menu item. Retrieve this value in 
      <a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a> 
      applications by getting the 
      <a href="/previous-versions/windows/desktop/mmc/menuitem-languageindependentname">MenuItem.LanguageIndependentName</a> 
      property. The <b>strLanguageIndependentName</b> member cannot be 
      <b>NULL</b> or an empty string unless a separator or insertion point is added; otherwise, 
      the <a href="/windows/desktop/api/mmc/nf-mmc-icontextmenucallback-additem">IContextMenuCallback::AddItem</a> method 
      will fail with <b>E_INVALIDARG</b> as the return value.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback2">IContextMenuCallback2</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>



<a href="/previous-versions/windows/desktop/mmc/working-with-context-menus">Working with Context Menus</a>