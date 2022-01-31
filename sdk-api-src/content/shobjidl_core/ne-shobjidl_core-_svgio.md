---
UID: NE:shobjidl_core._SVGIO
title: _SVGIO (shobjidl_core.h)
description: Used with the IFolderView::Items, IFolderView::ItemCount, and IShellView::GetItemObject methods to restrict or control the items in their collections.
helpviewer_keywords: ["SVGIO_ALLVIEW","SVGIO_BACKGROUND","SVGIO_CHECKED","SVGIO_FLAG_VIEWORDER","SVGIO_SELECTION","SVGIO_TYPE_MASK","_SVGIO","_SVGIO enumeration [Windows Shell]","_shell_SVGIO","shell.SVGIO","shobjidl_core/SVGIO_ALLVIEW","shobjidl_core/SVGIO_BACKGROUND","shobjidl_core/SVGIO_CHECKED","shobjidl_core/SVGIO_FLAG_VIEWORDER","shobjidl_core/SVGIO_SELECTION","shobjidl_core/SVGIO_TYPE_MASK","shobjidl_core/_SVGIO"]
old-location: shell\SVGIO.htm
tech.root: shell
ms.assetid: 06ed616b-8121-4ea0-bd05-632888d0f376
ms.date: 12/05/2018
ms.keywords: SVGIO_ALLVIEW, SVGIO_BACKGROUND, SVGIO_CHECKED, SVGIO_FLAG_VIEWORDER, SVGIO_SELECTION, SVGIO_TYPE_MASK, _SVGIO, _SVGIO enumeration [Windows Shell], _shell_SVGIO, shell.SVGIO, shobjidl_core/SVGIO_ALLVIEW, shobjidl_core/SVGIO_BACKGROUND, shobjidl_core/SVGIO_CHECKED, shobjidl_core/SVGIO_FLAG_VIEWORDER, shobjidl_core/SVGIO_SELECTION, shobjidl_core/SVGIO_TYPE_MASK, shobjidl_core/_SVGIO
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: _SVGIO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SVGIO
 - shobjidl_core/_SVGIO
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
 - _SVGIO
---

# _SVGIO enumeration


## -description

Used with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items">IFolderView::Items</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount">IFolderView::ItemCount</a>, and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject">IShellView::GetItemObject</a> methods to restrict or control the items in their collections.

## -enum-fields

### -field SVGIO_BACKGROUND:0

0x00000000. Refers to the background of the view. It is used with IID_IContextMenu to get a shortcut menu for the view background and with IID_IDispatch to get a dispatch interface that represents the <a href="/windows/desktop/shell/shellfolderview">ShellFolderView</a> object for the view.

### -field SVGIO_SELECTION:0x1

0x00000001. Refers to the currently selected items. Used with IID_IDataObject to retrieve a data object that represents the selected items.

### -field SVGIO_ALLVIEW:0x2

0x00000002. Used in the same way as <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svgio">SVGIO_SELECTION</a> but refers to all items in the view.

### -field SVGIO_CHECKED:0x3

0x00000003. Used in the same way as <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svgio">SVGIO_SELECTION</a> but refers to checked items in views where checked mode is supported. For more details on checked mode, see <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>.

### -field SVGIO_TYPE_MASK:0xf

0x0000000F. Masks all bits but those corresponding to the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svgio">_SVGIO</a> flags.

### -field SVGIO_FLAG_VIEWORDER:0x80000000

0x80000000. Returns the items in the order they appear in the view. If this flag is not set, the selected item will be listed first.

## -remarks

The <b>SVGIO</b> type used to refer to members of the <b>_SVGIO</b> enumeration is defined in Shobjidl.h as shown here.


```
typedef int SVGIO;
```
