---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetItemCustomState
title: INameSpaceTreeControl::GetItemCustomState (shobjidl_core.h)
description: Gets the state of the checkbox associated with a given Shell item.
helpviewer_keywords: ["GetItemCustomState","GetItemCustomState method [Windows Shell]","GetItemCustomState method [Windows Shell]","INameSpaceTreeControl interface","INameSpaceTreeControl interface [Windows Shell]","GetItemCustomState method","INameSpaceTreeControl.GetItemCustomState","INameSpaceTreeControl::GetItemCustomState","_shell_INameSpaceTreeControl_GetItemCustomState","shell.INameSpaceTreeControl_GetItemCustomState","shobjidl_core/INameSpaceTreeControl::GetItemCustomState"]
old-location: shell\INameSpaceTreeControl_GetItemCustomState.htm
tech.root: shell
ms.assetid: 16fb3e3a-1686-4bdf-9112-564bb85fb601
ms.date: 12/05/2018
ms.keywords: GetItemCustomState, GetItemCustomState method [Windows Shell], GetItemCustomState method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetItemCustomState method, INameSpaceTreeControl.GetItemCustomState, INameSpaceTreeControl::GetItemCustomState, _shell_INameSpaceTreeControl_GetItemCustomState, shell.INameSpaceTreeControl_GetItemCustomState, shobjidl_core/INameSpaceTreeControl::GetItemCustomState
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
 - INameSpaceTreeControl::GetItemCustomState
 - shobjidl_core/INameSpaceTreeControl::GetItemCustomState
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
 - INameSpaceTreeControl.GetItemCustomState
---

# INameSpaceTreeControl::GetItemCustomState


## -description

Gets the state of the checkbox associated with a given Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item for which checkbox state is being retrieved.

### -param piStateNumber [out]

Type: <b>int*</b>

A pointer to the state of the checkbox for the Shell item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.