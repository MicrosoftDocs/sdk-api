---
UID: NF:shobjidl_core.IContextMenu.QueryContextMenu
title: IContextMenu::QueryContextMenu (shobjidl_core.h)
description: Adds commands to a shortcut menu.
helpviewer_keywords: ["CMF_ASYNCVERBSTATE","CMF_CANRENAME","CMF_DEFAULTONLY","CMF_DISABLEDVERBS","CMF_DONOTPICKDEFAULT","CMF_EXPLORE","CMF_EXTENDEDVERBS","CMF_INCLUDESTATIC","CMF_ITEMMENU","CMF_NODEFAULT","CMF_NORMAL","CMF_NOVERBS","CMF_OPTIMIZEFORINVOKE","CMF_RESERVED","CMF_SYNCCASCADEMENU","CMF_VERBSONLY","IContextMenu interface [Windows Shell]","QueryContextMenu method","IContextMenu.QueryContextMenu","IContextMenu::QueryContextMenu","QueryContextMenu","QueryContextMenu method [Windows Shell]","QueryContextMenu method [Windows Shell]","IContextMenu interface","_win32_IContextMenu_QueryContextMenu","_win32_icontextmenu_win32_icontextmenu_querycontextmenu_cpp","shell.IContextMenu_QueryContextMenu","shobjidl_core/IContextMenu::QueryContextMenu"]
old-location: shell\IContextMenu_QueryContextMenu.htm
tech.root: shell
ms.assetid: 329fe15b-c1c1-4ffd-812e-9e74451bad6e
ms.date: 12/05/2018
ms.keywords: CMF_ASYNCVERBSTATE, CMF_CANRENAME, CMF_DEFAULTONLY, CMF_DISABLEDVERBS, CMF_DONOTPICKDEFAULT, CMF_EXPLORE, CMF_EXTENDEDVERBS, CMF_INCLUDESTATIC, CMF_ITEMMENU, CMF_NODEFAULT, CMF_NORMAL, CMF_NOVERBS, CMF_OPTIMIZEFORINVOKE, CMF_RESERVED, CMF_SYNCCASCADEMENU, CMF_VERBSONLY, IContextMenu interface [Windows Shell],QueryContextMenu method, IContextMenu.QueryContextMenu, IContextMenu::QueryContextMenu, QueryContextMenu, QueryContextMenu method [Windows Shell], QueryContextMenu method [Windows Shell],IContextMenu interface, _win32_IContextMenu_QueryContextMenu, _win32_icontextmenu_win32_icontextmenu_querycontextmenu_cpp, shell.IContextMenu_QueryContextMenu, shobjidl_core/IContextMenu::QueryContextMenu
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenu::QueryContextMenu
 - shobjidl_core/IContextMenu::QueryContextMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IContextMenu.QueryContextMenu
---

# IContextMenu::QueryContextMenu


## -description

Adds commands to a shortcut menu.

## -parameters

### -param hmenu

Type: <b>HMENU</b>

A handle to the shortcut menu. The handler should specify this handle when adding menu items.

### -param indexMenu

Type: <b>UINT</b>

The zero-based position at which to insert the first new menu item.

### -param idCmdFirst

Type: <b>UINT</b>

The minimum value that the handler can specify for a menu item identifier.

### -param idCmdLast

Type: <b>UINT</b>

The maximum value that the handler can specify for a menu item identifier.

### -param uFlags

Type: <b>UINT</b>

Optional flags that specify how the shortcut menu can be changed. This parameter can be set to a combination of the following values. The remaining bits of the low-order word are reserved by the system. The high-order word can be used for context-specific communications. The CMF_RESERVED value can be used to mask the low-order word.



#### CMF_NORMAL (0x00000000)

0x00000000. Indicates normal operation. A shortcut menu extension, namespace extension, or drag-and-drop handler can add all menu items.



#### CMF_DEFAULTONLY (0x00000001)

0x00000001. The user is activating the default action, typically by double-clicking. This flag provides a hint for the shortcut menu extension to add nothing if it does not modify the default item in the menu. A shortcut menu extension or drag-and-drop handler should not add any menu items if this value is specified. A namespace extension should at most add only the default item.



#### CMF_VERBSONLY (0x00000002)

0x00000002. The shortcut menu is that of a shortcut file (normally, a .lnk file). Shortcut menu handlers should ignore this value.



#### CMF_EXPLORE (0x00000004)

0x00000004. The Windows Explorer tree window is present.



#### CMF_NOVERBS (0x00000008)

0x00000008. This flag is set for items displayed in the <b>Send To</b> menu. Shortcut menu handlers should ignore this value.



#### CMF_CANRENAME (0x00000010)

0x00000010. The calling application supports renaming of items. A shortcut menu or drag-and-drop handler should ignore this flag. A namespace extension should add a <b>Rename</b> item to the menu if applicable.



#### CMF_NODEFAULT (0x00000020)

0x00000020. No item in the menu has been set as the default. A drag-and-drop handler should ignore this flag. A namespace extension should not set any of the menu items as the default.



#### CMF_INCLUDESTATIC (0x00000040)

This value is not available.

<b>Windows Server 2003 and Windows XP:</b> 0x00000040. A static menu is being constructed. Only the browser should use this flag; all other shortcut menu extensions should ignore it.



#### CMF_ITEMMENU (0x00000080)

0x00000080. The calling application is invoking a shortcut menu on an item in the view (as opposed to the background of the view).

<b>Windows Server 2003 and Windows XP:  </b>This value is not available.



#### CMF_EXTENDEDVERBS (0x00000100)

0x00000100. The calling application wants extended verbs. Normal verbs are displayed when the user right-clicks an object. To display extended verbs, the user must right-click while pressing the Shift key.



#### CMF_DISABLEDVERBS (0x00000200)

0x00000200. The calling application intends to invoke verbs that are disabled, such as legacy menus.

<b>Windows Server 2003 and Windows XP:  </b>This value is not available.



#### CMF_ASYNCVERBSTATE (0x00000400)

0x00000400. The verb state can be evaluated asynchronously.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.



#### CMF_OPTIMIZEFORINVOKE (0x00000800)

0x00000800. Informs context menu handlers that do not support the invocation of a verb through a canonical verb name to bypass <b>IContextMenu::QueryContextMenu</b> in their implementation.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.



#### CMF_SYNCCASCADEMENU (0x00001000)

0x00001000. Populate submenus synchronously.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.



#### CMF_DONOTPICKDEFAULT (0x00002000)

0x00002000. When no verb is explicitly specified, do not use a default verb in its place.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.



#### CMF_RESERVED (0xffff0000)

0xffff0000. This flag is a bitmask that specifies all bits that should not be used. This is to be used only as a mask. Do not pass this as a parameter value.

## -returns

Type: <b>HRESULT</b>

If successful, returns an <b>HRESULT</b> value that has its severity value set to SEVERITY_SUCCESS and its code value set to the offset of the largest command identifier that was assigned, plus one. For example, if <i>idCmdFirst</i> is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8, the return value should be MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1). Otherwise, it returns a COM error value.

## -remarks

This method should call either <a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a> or <a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a> to insert its menu items into the menu specified by <i>hmenu</i>. The <i>indexMenu</i> parameter holds the index to be used for the first menu item. The identifier of each menu item must fall within the range defined by <i>idCmdFirst</i> and <i>idCmdLast</i>.

A common practice is to set the first command identifier to <i>idCmdFirst</i> (an offset of zero) and increment the offset for each additional command by one. This practice ensures that you do not exceed <i>idCmdLast</i> and preserves the range of identifiers that are available for use by other handlers. Store the offsets for reference because they can be used to identify the command in subsequent calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring">IContextMenu::GetCommandString</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a>.

If the Shell subsequently calls another shortcut menu handler, it will use the code value of the returned <b>HRESULT</b> to set <i>idCmdFirst</i> when it calls that handler's <b>QueryContextMenu</b> method.

When a context menu handler adds a pop-up menu item, it must use <b>IContextMenu::QueryContextMenu</b> to add at least one item to that menu for the WM_INITMENUPOPUP message to be forwarded.
