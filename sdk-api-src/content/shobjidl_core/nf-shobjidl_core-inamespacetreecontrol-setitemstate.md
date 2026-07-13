---
UID: NF:shobjidl_core.INameSpaceTreeControl.SetItemState
title: INameSpaceTreeControl::SetItemState (shobjidl_core.h)
description: Sets state information for a Shell item.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","SetItemState method","INameSpaceTreeControl.SetItemState","INameSpaceTreeControl::SetItemState","SetItemState","SetItemState method [Windows Shell]","SetItemState method [Windows Shell]","INameSpaceTreeControl interface","_shell_INameSpaceTreeControl_SetItemState","shell.INameSpaceTreeControl_SetItemState","shobjidl_core/INameSpaceTreeControl::SetItemState"]
old-location: shell\INameSpaceTreeControl_SetItemState.htm
tech.root: shell
ms.assetid: f57c5abc-0803-409d-9938-3826f9d8058d
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],SetItemState method, INameSpaceTreeControl.SetItemState, INameSpaceTreeControl::SetItemState, SetItemState, SetItemState method [Windows Shell], SetItemState method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_SetItemState, shell.INameSpaceTreeControl_SetItemState, shobjidl_core/INameSpaceTreeControl::SetItemState
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
 - INameSpaceTreeControl::SetItemState
 - shobjidl_core/INameSpaceTreeControl::SetItemState
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
 - INameSpaceTreeControl.SetItemState
---

# INameSpaceTreeControl::SetItemState


## -description

Sets state information for a Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item for which to set the state.

### -param nstcisMask [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

Specifies which information is being set, in the form of a bitmap. One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a> constants.

### -param nstcisFlags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

A bitmap that contains the values to set for the flags specified in <i>nstcisMask</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>nstcisMask</i> value specifies which bits in the value pointed to by <i>pnstcisFlags</i> are to be set. Other bits are ignored. As a simple example, if <i>nstcisMask</i>=NSTCIS_SELECTED, then the first bit in the <i>nstcisFlags</i> value determines whether that flag is set (1) or removed (0).