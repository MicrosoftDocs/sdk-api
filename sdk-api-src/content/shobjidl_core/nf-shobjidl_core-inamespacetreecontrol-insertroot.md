---
UID: NF:shobjidl_core.INameSpaceTreeControl.InsertRoot
title: INameSpaceTreeControl::InsertRoot (shobjidl_core.h)
description: Inserts a Shell item on a root item in a tree.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","InsertRoot method","INameSpaceTreeControl.InsertRoot","INameSpaceTreeControl::InsertRoot","InsertRoot","InsertRoot method [Windows Shell]","InsertRoot method [Windows Shell]","INameSpaceTreeControl interface","NSTCRS_EXPANDED","NSTCRS_HIDDEN","NSTCRS_VISIBLE","_shell_INameSpaceTreeControl_InsertRoot","shell.INameSpaceTreeControl_InsertRoot","shobjidl_core/INameSpaceTreeControl::InsertRoot"]
old-location: shell\INameSpaceTreeControl_InsertRoot.htm
tech.root: shell
ms.assetid: 5d487896-a2ee-4bf3-82d8-90f23a4ff213
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],InsertRoot method, INameSpaceTreeControl.InsertRoot, INameSpaceTreeControl::InsertRoot, InsertRoot, InsertRoot method [Windows Shell], InsertRoot method [Windows Shell],INameSpaceTreeControl interface, NSTCRS_EXPANDED, NSTCRS_HIDDEN, NSTCRS_VISIBLE, _shell_INameSpaceTreeControl_InsertRoot, shell.INameSpaceTreeControl_InsertRoot, shobjidl_core/INameSpaceTreeControl::InsertRoot
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INameSpaceTreeControl::InsertRoot
 - shobjidl_core/INameSpaceTreeControl::InsertRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.InsertRoot
---

# INameSpaceTreeControl::InsertRoot


## -description

Inserts a Shell item on a root item in a tree.

## -parameters

### -param iIndex [in]

Type: <b>int</b>

The index at which to insert the root.

### -param psiRoot [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item that is being inserted.

### -param grfEnumFlags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a></b>

Enumerates the qualities of the root and all of its children. One of the values of type <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a>.

### -param grfRootStyle [in]

Type: <b>NSTCROOTSTYLE</b>

The style of the root that is being inserted. One or more of the following values (flags can be combined using a bitwise OR).



#### NSTCRS_VISIBLE (0x0000)

The root is visible as well as the items.  Mutually exclusive with NSTCRS_HIDDEN.



#### NSTCRS_HIDDEN (0x0001)

The root is hidden so that only the children are visible. Mutually exclusive with NSTCRS_VISIBLE.



#### NSTCRS_EXPANDED (0x0002)

The root is expanded upon initialization.

### -param pif [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a> that enables you to filter which items in the tree are displayed. If supplied, every item is customizable with a <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a> flag. This value can be <b>NULL</b> if no filter is required.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.