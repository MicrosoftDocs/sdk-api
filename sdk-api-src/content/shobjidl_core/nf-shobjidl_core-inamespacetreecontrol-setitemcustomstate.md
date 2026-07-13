---
UID: NF:shobjidl_core.INameSpaceTreeControl.SetItemCustomState
title: INameSpaceTreeControl::SetItemCustomState (shobjidl_core.h)
description: Sets the state of the checkbox associated with the Shell item.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","SetItemCustomState method","INameSpaceTreeControl.SetItemCustomState","INameSpaceTreeControl::SetItemCustomState","SetItemCustomState","SetItemCustomState method [Windows Shell]","SetItemCustomState method [Windows Shell]","INameSpaceTreeControl interface","_shell_INameSpaceTreeControl_SetItemCustomState","shell.INameSpaceTreeControl_SetItemCustomState","shobjidl_core/INameSpaceTreeControl::SetItemCustomState"]
old-location: shell\INameSpaceTreeControl_SetItemCustomState.htm
tech.root: shell
ms.assetid: a27fa2a3-3e10-4053-b0b6-222c7b517b5a
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],SetItemCustomState method, INameSpaceTreeControl.SetItemCustomState, INameSpaceTreeControl::SetItemCustomState, SetItemCustomState, SetItemCustomState method [Windows Shell], SetItemCustomState method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_SetItemCustomState, shell.INameSpaceTreeControl_SetItemCustomState, shobjidl_core/INameSpaceTreeControl::SetItemCustomState
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
 - INameSpaceTreeControl::SetItemCustomState
 - shobjidl_core/INameSpaceTreeControl::SetItemCustomState
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
 - INameSpaceTreeControl.SetItemCustomState
---

# INameSpaceTreeControl::SetItemCustomState


## -description

Sets the state of the checkbox associated with the Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item for which checkbox state
                is being set.

### -param iStateNumber [in]

Type: <b>int</b>

The desired state of the checkbox for the Shell item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.