---
UID: NF:shobjidl_core.IExplorerCommand.GetState
title: IExplorerCommand::GetState (shobjidl_core.h)
description: Gets state information associated with a specified Windows Explorer command item.
helpviewer_keywords: ["GetState","GetState method [Windows Shell]","GetState method [Windows Shell]","IExplorerCommand interface","IExplorerCommand interface [Windows Shell]","GetState method","IExplorerCommand.GetState","IExplorerCommand::GetState","_shell_IExplorerCommand_GetState","shell.IExplorerCommand_GetState","shobjidl_core/IExplorerCommand::GetState"]
old-location: shell\IExplorerCommand_GetState.htm
tech.root: shell
ms.assetid: bb600cb5-9b7e-45dc-beca-0a913c214084
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetState method, IExplorerCommand.GetState, IExplorerCommand::GetState, _shell_IExplorerCommand_GetState, shell.IExplorerCommand_GetState, shobjidl_core/IExplorerCommand::GetState
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
 - IExplorerCommand::GetState
 - shobjidl_core/IExplorerCommand::GetState
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
 - IExplorerCommand.GetState
---

# IExplorerCommand::GetState


## -description

Gets state information associated with a specified Windows Explorer command item.

## -parameters

### -param psiItemArray [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

### -param fOkToBeSlow [in]

Type: <b>BOOL</b>

<b>FALSE</b> if a verb object should not perform any memory intensive computations that could cause the UI thread to stop responding. The verb object should return E_PENDING in that case. If <b>TRUE</b>, those computations can be completed.

### -param pCmdState [out]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_expcmdstate">EXPCMDSTATE</a>*</b>

A pointer to a value that, when this method returns successfully, receives one or more Windows Explorer command states indicated by the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_expcmdstate">EXPCMDSTATE</a> constants.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.