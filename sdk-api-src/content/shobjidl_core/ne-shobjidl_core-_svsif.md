---
UID: NE:shobjidl_core._SVSIF
title: _SVSIF (shobjidl_core.h)
description: Indicates flags used by IFolderView, IFolderView2, IShellView and IShellView2 to specify a type of selection to apply.
helpviewer_keywords: ["SVSI_CHECK","SVSI_CHECK2","SVSI_DESELECT","SVSI_DESELECTOTHERS","SVSI_EDIT","SVSI_ENSUREVISIBLE","SVSI_FOCUSED","SVSI_KEYBOARDSELECT","SVSI_NOTAKEFOCUS","SVSI_POSITIONITEM","SVSI_SELECT","SVSI_SELECTIONMARK","SVSI_TRANSLATEPT","_SVSIF","_SVSIF enumeration [Windows Shell]","_shell_SVSIF","shell.SVSIF","shobjidl_core/SVSI_CHECK","shobjidl_core/SVSI_CHECK2","shobjidl_core/SVSI_DESELECT","shobjidl_core/SVSI_DESELECTOTHERS","shobjidl_core/SVSI_EDIT","shobjidl_core/SVSI_ENSUREVISIBLE","shobjidl_core/SVSI_FOCUSED","shobjidl_core/SVSI_KEYBOARDSELECT","shobjidl_core/SVSI_NOTAKEFOCUS","shobjidl_core/SVSI_POSITIONITEM","shobjidl_core/SVSI_SELECT","shobjidl_core/SVSI_SELECTIONMARK","shobjidl_core/SVSI_TRANSLATEPT","shobjidl_core/_SVSIF"]
old-location: shell\SVSIF.htm
tech.root: shell
ms.assetid: 3b0a7ec3-f365-48ec-86b0-ffd4c345deaf
ms.date: 12/05/2018
ms.keywords: SVSI_CHECK, SVSI_CHECK2, SVSI_DESELECT, SVSI_DESELECTOTHERS, SVSI_EDIT, SVSI_ENSUREVISIBLE, SVSI_FOCUSED, SVSI_KEYBOARDSELECT, SVSI_NOTAKEFOCUS, SVSI_POSITIONITEM, SVSI_SELECT, SVSI_SELECTIONMARK, SVSI_TRANSLATEPT, _SVSIF, _SVSIF enumeration [Windows Shell], _shell_SVSIF, shell.SVSIF, shobjidl_core/SVSI_CHECK, shobjidl_core/SVSI_CHECK2, shobjidl_core/SVSI_DESELECT, shobjidl_core/SVSI_DESELECTOTHERS, shobjidl_core/SVSI_EDIT, shobjidl_core/SVSI_ENSUREVISIBLE, shobjidl_core/SVSI_FOCUSED, shobjidl_core/SVSI_KEYBOARDSELECT, shobjidl_core/SVSI_NOTAKEFOCUS, shobjidl_core/SVSI_POSITIONITEM, shobjidl_core/SVSI_SELECT, shobjidl_core/SVSI_SELECTIONMARK, shobjidl_core/SVSI_TRANSLATEPT, shobjidl_core/_SVSIF
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: _SVSIF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SVSIF
 - shobjidl_core/_SVSIF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - _SVSIF
---

# _SVSIF enumeration


## -description

Indicates flags used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> and  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2">IShellView2</a> to specify a type of selection to apply.

## -enum-fields

### -field SVSI_DESELECT:0

0x00000000. Deselect the item.

### -field SVSI_SELECT:0x1

0x00000001. Select the item.

### -field SVSI_EDIT:0x3

0x00000003. Put the name of the item into rename mode. This value includes SVSI_SELECT.

### -field SVSI_DESELECTOTHERS:0x4

0x00000004. Deselect all but the selected item. If the item parameter is <b>NULL</b>, deselect all items.

### -field SVSI_ENSUREVISIBLE:0x8

0x00000008. In the case of a folder that cannot display all of its contents on one screen, display the portion that contains the selected item.

### -field SVSI_FOCUSED:0x10

0x00000010. Give the selected item the focus when multiple items are selected, placing the item first in any list of the collection returned by a method.

### -field SVSI_TRANSLATEPT:0x20

0x00000020. Convert the input point from screen coordinates to the list-view client coordinates.

### -field SVSI_SELECTIONMARK:0x40

0x00000040. Mark the item so that it can be queried using <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getselectionmarkeditem">IFolderView::GetSelectionMarkedItem</a>.

### -field SVSI_POSITIONITEM:0x80

0x00000080. Allows the window's default view to position the item. In most cases, this will place the item in the first available position. However, if the call comes during the processing of a mouse-positioned context menu, the position of the context menu is used to position the item.

### -field SVSI_CHECK:0x100

0x00000100. The item should be checked. This flag is used with items in views where the checked mode is supported.

### -field SVSI_CHECK2:0x200

0x00000200. The second check state when the view is in tri-check mode, in which there are three values for the checked state. You can indicate tri-check mode by specifying FWF_TRICHECKSELECT in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-setcurrentfolderflags">IFolderView2::SetCurrentFolderFlags</a>. The 3 states for FWF_TRICHECKSELECT are unchecked, SVSI_CHECK and SVSI_CHECK2.

### -field SVSI_KEYBOARDSELECT:0x401

0x00000401. Selects the item and marks it as selected by the keyboard. This value includes SVSI_SELECT.

### -field SVSI_NOTAKEFOCUS:0x40000000

0x40000000. An operation to select or focus an item should not also set focus on the view itself.

## -remarks

An additional value SVSI_NOSTATECHANGE is also defined outside of the enumeration. This value indicates that an operation to edit or position an item should not affect the item's focus or selected state. Its numeric value is (UINT)0x80000000.

The <b>SVSIF</b> type used to refer to members of the <b>_SVSIF</b> enumeration is defined in Shobjidl.h as shown here.

                


```
typedef UINT SVSIF;
```
