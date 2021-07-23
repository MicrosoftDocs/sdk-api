---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetNextItem
title: INameSpaceTreeControl::GetNextItem (shobjidl_core.h)
description: Retrieves the next item in the tree according to which method is requested.
helpviewer_keywords: ["GetNextItem","GetNextItem method [Windows Shell]","GetNextItem method [Windows Shell]","INameSpaceTreeControl interface","INameSpaceTreeControl interface [Windows Shell]","GetNextItem method","INameSpaceTreeControl.GetNextItem","INameSpaceTreeControl::GetNextItem","NSTCGNI_CHILD","NSTCGNI_FIRSTVISIBLE","NSTCGNI_LASTVISIBLE","NSTCGNI_NEXT","NSTCGNI_NEXTVISIBLE","NSTCGNI_PARENT","NSTCGNI_PREV","NSTCGNI_PREVVISIBLE","_shell_INameSpaceTreeControl_GetNextItem","shell.INameSpaceTreeControl_GetNextItem","shobjidl_core/INameSpaceTreeControl::GetNextItem"]
old-location: shell\INameSpaceTreeControl_GetNextItem.htm
tech.root: shell
ms.assetid: 71ede595-14b6-4e59-854a-af75c02093f8
ms.date: 12/05/2018
ms.keywords: GetNextItem, GetNextItem method [Windows Shell], GetNextItem method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetNextItem method, INameSpaceTreeControl.GetNextItem, INameSpaceTreeControl::GetNextItem, NSTCGNI_CHILD, NSTCGNI_FIRSTVISIBLE, NSTCGNI_LASTVISIBLE, NSTCGNI_NEXT, NSTCGNI_NEXTVISIBLE, NSTCGNI_PARENT, NSTCGNI_PREV, NSTCGNI_PREVVISIBLE, _shell_INameSpaceTreeControl_GetNextItem, shell.INameSpaceTreeControl_GetNextItem, shobjidl_core/INameSpaceTreeControl::GetNextItem
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
 - INameSpaceTreeControl::GetNextItem
 - shobjidl_core/INameSpaceTreeControl::GetNextItem
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
 - INameSpaceTreeControl.GetNextItem
---

# INameSpaceTreeControl::GetNextItem


## -description

Retrieves the next item in the tree according to which method is requested.

## -parameters

### -param psi [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

The Shell item for which the next item is being retrieved. This value can be <b>NULL</b>.

### -param nstcgi [in]

Type: <b>NSTCGNI</b>

The type of the next item. This value can be one of the following flags:



#### NSTCGNI_NEXT (0)

The next sibling of the given item.



#### NSTCGNI_NEXTVISIBLE (1)

The next visible item in the tree that has any relationship to the given item. This includes a child (if there is one), the next sibling, or even one of the ancestor's siblings.



#### NSTCGNI_PREV (2)

The previous sibling item of the given item.



#### NSTCGNI_PREVVISIBLE (3)

The previous visible item that is a sibling item, sibling descendent item or a parent item.



#### NSTCGNI_PARENT (4)

The parent item of the given item.



#### NSTCGNI_CHILD (5)

The first child item of the given item.



#### NSTCGNI_FIRSTVISIBLE (6)

The absolute first visible item in the tree (not relative to the given item).



#### NSTCGNI_LASTVISIBLE (7)

The absolute last visible item in the tree (not relative to the given item).

### -param ppsiNext [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that fits the criteria for the next item that was requested.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If there is no next item for the type selected, this function returns E_FAIL with <b>NULL</b> for the returned item, <i>ppsiNext</i>.