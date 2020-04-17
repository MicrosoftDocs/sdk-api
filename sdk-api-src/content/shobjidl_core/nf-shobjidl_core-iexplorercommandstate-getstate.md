---
UID: NF:shobjidl_core.IExplorerCommandState.GetState
title: IExplorerCommandState::GetState (shobjidl_core.h)
description: Gets the command state associated with a specified Shell item.helpviewer_keywords: ["GetState","GetState method [Windows Shell]","GetState method [Windows Shell]","IExplorerCommandState interface","IExplorerCommandState interface [Windows Shell]","GetState method","IExplorerCommandState.GetState","IExplorerCommandState::GetState","_shell_IExplorerCommandState_GetState","shell.IExplorerCommandState_GetState","shobjidl_core/IExplorerCommandState::GetState"]
old-location: shell\IExplorerCommandState_GetState.htm
tech.root: shell
ms.assetid: a93bc6af-bea3-48c1-b3bd-a2bb2a0582a7
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IExplorerCommandState interface, IExplorerCommandState interface [Windows Shell],GetState method, IExplorerCommandState.GetState, IExplorerCommandState::GetState, _shell_IExplorerCommandState_GetState, shell.IExplorerCommandState_GetState, shobjidl_core/IExplorerCommandState::GetState
f1_keywords:
- shobjidl_core/IExplorerCommandState.GetState
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IExplorerCommandState.GetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerCommandState::GetState


## -description


Gets the command state associated with a specified Shell item.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> with a single element that represents the Shell item.


### -param fOkToBeSlow [in]

Type: <b>BOOL</b>

<b>FALSE</b> if a verb object should not perform any memory intensive computations that could cause the UI thread to stop responding. The verb object should return E_PENDING in that case. If <b>TRUE</b>, those computations can be completed.


### -param pCmdState [out]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/shobjidl_core/ne-shobjidl_core-_expcmdstate">EXPCMDSTATE</a>*</b>

A pointer to a value that, when this method returns successfully, receives one or more Windows Explorer command states indicated by the <a href="https://docs.microsoft.com/windows/win32/api/shobjidl_core/ne-shobjidl_core-_expcmdstate">EXPCMDSTATE</a> constants.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method provides the same functionality as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getstate">GetState</a>. Use <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate">IExplorerCommandState</a> when you only need to know the command state.



