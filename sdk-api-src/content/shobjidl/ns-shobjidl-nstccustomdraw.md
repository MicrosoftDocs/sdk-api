---
UID: NS:shobjidl.NSTCCUSTOMDRAW
title: NSTCCUSTOMDRAW (shobjidl.h)
description: Custom draw structure used by INameSpaceTreeControlCustomDraw methods.
helpviewer_keywords: ["NSTCCUSTOMDRAW","NSTCCUSTOMDRAW structure [Windows Shell]","_shell_NSTCCUSTOMDRAW","shell.NSTCCUSTOMDRAW","shobjidl/NSTCCUSTOMDRAW"]
old-location: shell\NSTCCUSTOMDRAW.htm
tech.root: shell
ms.assetid: 95747075-4882-4c29-8653-941ac04db54b
ms.date: 12/05/2018
ms.keywords: NSTCCUSTOMDRAW, NSTCCUSTOMDRAW structure [Windows Shell], _shell_NSTCCUSTOMDRAW, shell.NSTCCUSTOMDRAW, shobjidl/NSTCCUSTOMDRAW
req.header: shobjidl.h
req.include-header: 
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
req.typenames: NSTCCUSTOMDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NSTCCUSTOMDRAW
 - shobjidl/NSTCCUSTOMDRAW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - NSTCCUSTOMDRAW
---

# NSTCCUSTOMDRAW structure


## -description

Custom draw structure used by <a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw">INameSpaceTreeControlCustomDraw</a> methods.

## -struct-fields

### -field psi

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to a Shell item.

### -field uItemState

Type: <b>UINT</b>

The current item state. See <a href="/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw">NMCUSTOMDRAW</a> for more detail.

### -field nstcis

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

The state of a tree item. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a>.

### -field pszText

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that contains the item text, if the structure specifies item attributes.

### -field iImage

Type: <b>int</b>

The index in the tree-view control's image list.

### -field himl

Type: <b>HIMAGELIST</b>

A handle to an image list.

### -field iLevel

Type: <b>int</b>

The zero-based level of the item being drawn.

### -field iIndent

Type: <b>int</b>

A tree-level indent.