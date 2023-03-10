---
UID: NF:shobjidl_core.IContextMenuSite.DoContextMenuPopup
title: IContextMenuSite::DoContextMenuPopup (shobjidl_core.h)
description: DoContextMenuPopup is no longer available for use as of Windows Server 2003.
helpviewer_keywords: ["CMF_ASYNCVERBSTATE","CMF_CANRENAME","CMF_DEFAULTONLY","CMF_DISABLEDVERBS","CMF_DONOTPICKDEFAULT","CMF_EXPLORE","CMF_EXTENDEDVERBS","CMF_INCLUDESTATIC","CMF_ITEMMENU","CMF_NODEFAULT","CMF_NORMAL","CMF_NOVERBS","CMF_OPTIMIZEFORINVOKE","CMF_RESERVED","CMF_SYNCCASCADEMENU","CMF_VERBSONLY","DoContextMenuPopup","DoContextMenuPopup method [Windows Shell]","DoContextMenuPopup method [Windows Shell]","IContextMenuSite interface","IContextMenuSite interface [Windows Shell]","DoContextMenuPopup method","IContextMenuSite.DoContextMenuPopup","IContextMenuSite::DoContextMenuPopup","_shell_IContextMenuSite_DoContextMenuPopup","shell.IContextMenuSite_DoContextMenuPopup","shobjidl_core/IContextMenuSite::DoContextMenuPopup"]
old-location: shell\IContextMenuSite_DoContextMenuPopup.htm
tech.root: shell
ms.assetid: 5601dc9c-e008-4387-b0d3-4cbdf29b7849
ms.date: 12/05/2018
ms.keywords: CMF_ASYNCVERBSTATE, CMF_CANRENAME, CMF_DEFAULTONLY, CMF_DISABLEDVERBS, CMF_DONOTPICKDEFAULT, CMF_EXPLORE, CMF_EXTENDEDVERBS, CMF_INCLUDESTATIC, CMF_ITEMMENU, CMF_NODEFAULT, CMF_NORMAL, CMF_NOVERBS, CMF_OPTIMIZEFORINVOKE, CMF_RESERVED, CMF_SYNCCASCADEMENU, CMF_VERBSONLY, DoContextMenuPopup, DoContextMenuPopup method [Windows Shell], DoContextMenuPopup method [Windows Shell],IContextMenuSite interface, IContextMenuSite interface [Windows Shell],DoContextMenuPopup method, IContextMenuSite.DoContextMenuPopup, IContextMenuSite::DoContextMenuPopup, _shell_IContextMenuSite_DoContextMenuPopup, shell.IContextMenuSite_DoContextMenuPopup, shobjidl_core/IContextMenuSite::DoContextMenuPopup
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenuSite::DoContextMenuPopup
 - shobjidl_core/IContextMenuSite::DoContextMenuPopup
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
 - IContextMenuSite.DoContextMenuPopup
---

# IContextMenuSite::DoContextMenuPopup


## -description

<p class="CCE_Message">[<b>DoContextMenuPopup</b> is no longer available for use as of Windows Server 2003.]

Creates and displays a shortcut menu, tracks the selection of items on that menu, and invokes a chosen command.

## -parameters

### -param punkContextMenu [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the shortcut menu's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation.

### -param fFlags [in]

Type: <b>UINT</b>

Optional flags specifying how the shortcut menu can be changed. This parameter can be set to any combination of the following values. The remaining bits of the low-order word are reserved by the system. The high-order word can be used for context-specific communications. The CMF_RESERVED value can be used to mask out the low-order word.



#### CMF_NORMAL (0x00000000)

0x00000000. Indicates normal operation. A shortcut menu extension, namespace extension, or drag-and-drop handler can add all menu items.



#### CMF_DEFAULTONLY (0x00000001)

0x00000001. This flag is set when the user is activating the default action, typically by double-clicking. This flag provides a hint for the shortcut menu extension to add nothing if it does not modify the default item in the menu. A shortcut menu extension or drag-and-drop handler should not add any menu items if this value is specified. A namespace extension should add only the default item (if any).



#### CMF_VERBSONLY (0x00000002)

0x00000002. This flag is set if the shortcut menu is for a shortcut object. Shortcut menu handlers should ignore this value.



#### CMF_EXPLORE (0x00000004)

0x00000004. This flag is set when the Windows Explorer tree window is present.



#### CMF_NOVERBS (0x00000008)

0x00000008. This flag is set for items displayed in the <b>Send To</b> menu. Shortcut menu handlers should ignore this value.



#### CMF_CANRENAME (0x00000010)

0x00000010. This flag is set if the calling application supports renaming of items. A shortcut menu extension or drag-and-drop handler should ignore this flag. A namespace extension should add a rename item to the menu if applicable.



#### CMF_NODEFAULT (0x00000020)

0x00000020. This flag is set if no item in the menu has been set as the default. A drag-and-drop handler should ignore this flag. A namespace extension should not set any of the menu items to the default.



#### CMF_INCLUDESTATIC (0x00000040)

This value is not available.

<b>Windows Server 2003 and Windows XP:</b> 0x00000040. This flag is set when a static menu is being constructed. Only the browser should use this flag. All other shortcut menu extensions should ignore this flag.



#### CMF_ITEMMENU (0x00000080)

0x00000080. This flag is set when the calling application is invoking a context menu on an item in the view (as opposed to the background of the view).

<b>Windows Server 2003 and Windows XP:</b> This value is not available.



#### CMF_EXTENDEDVERBS (0x00000100)

0x00000100. This flag is set when the calling application wants extended verbs. Normal verbs are displayed when the user right-clicks an object. To display extended verbs, the user must right-click while pressing the SHIFT key.



#### CMF_DISABLEDVERBS (0x00000200)

0x00000200. This flag is set when the calling application intends to invoke verbs that are otherwise disabled, such as legacy menus.

<b>Windows Server 2003 and Windows XP:</b> This value is not available.



#### CMF_ASYNCVERBSTATE (0x00000400)

0x00000400. This flag is set if the verb state can be evaluated asynchronously.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:</b> This value is not available.



#### CMF_OPTIMIZEFORINVOKE (0x00000800)

0x00000800. Informs context menu handlers that do not support the invocation of a verb through a canonical verb name to bypass that processing in their <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu">IContextMenu::QueryContextMenu</a> implementation.


<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:</b> This value is not available.



#### CMF_SYNCCASCADEMENU (0x00001000)

0x00001000. 

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:</b> This value is not available.



#### CMF_DONOTPICKDEFAULT (0x00002000)

0x00001000. When no verb is explicitly specified, do not use a default verb in its place.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:</b> This value is not available.



#### CMF_RESERVED (0xffff0000)

0xffff0000. This flag is a bitmask that specifies all bits that should not be used. This is to be used only as a mask. Do not pass this as a parameter value.

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Location where you want the shortcut menu to appear. This point specifies the location of the menu's upper left corner in screen coordinates.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.