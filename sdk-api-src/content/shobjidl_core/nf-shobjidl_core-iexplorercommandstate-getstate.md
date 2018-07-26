---
UID: NF:shobjidl_core.IExplorerCommandState.GetState
title: IExplorerCommandState::GetState
author: windows-sdk-content
description: Gets the command state associated with a specified Shell item.
old-location: shell\IExplorerCommandState_GetState.htm
old-project: shell
ms.assetid: a93bc6af-bea3-48c1-b3bd-a2bb2a0582a7
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IExplorerCommandState interface, IExplorerCommandState interface [Windows Shell],GetState method, IExplorerCommandState.GetState, IExplorerCommandState::GetState, _shell_IExplorerCommandState_GetState, shell.IExplorerCommandState_GetState, shobjidl_core/IExplorerCommandState::GetState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerCommandState.GetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerCommandState::GetState


## -description


Gets the command state associated with a specified Shell item.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a> with a single element that represents the Shell item.


### -param fOkToBeSlow [in]

Type: <b>BOOL</b>

<b>FALSE</b> if a verb object should not perform any memory intensive computations that could cause the UI thread to stop responding. The verb object should return E_PENDING in that case. If <b>TRUE</b>, those computations can be completed.


### -param pCmdState [out]

Type: <b><a href="https://msdn.microsoft.com/41e76b6e-9294-40b3-bb8b-bbfe487fd023">EXPCMDSTATE</a>*</b>

A pointer to a value that, when this method returns successfully, receives one or more Windows Explorer command states indicated by the <a href="https://msdn.microsoft.com/41e76b6e-9294-40b3-bb8b-bbfe487fd023">EXPCMDSTATE</a> constants.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method provides the same functionality as <a href="https://msdn.microsoft.com/bb600cb5-9b7e-45dc-beca-0a913c214084">GetState</a>. Use <a href="https://msdn.microsoft.com/020a6f6f-1d45-44bd-a57f-ef8000976b5b">IExplorerCommandState</a> when you only need to know the command state.



