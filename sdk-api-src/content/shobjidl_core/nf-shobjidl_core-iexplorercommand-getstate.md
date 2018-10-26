---
UID: NF:shobjidl_core.IExplorerCommand.GetState
title: IExplorerCommand::GetState
author: windows-sdk-content
description: Gets state information associated with a specified Windows Explorer command item.
old-location: shell\IExplorerCommand_GetState.htm
tech.root: shell
ms.assetid: bb600cb5-9b7e-45dc-beca-0a913c214084
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetState method, IExplorerCommand.GetState, IExplorerCommand::GetState, _shell_IExplorerCommand_GetState, shell.IExplorerCommand_GetState, shobjidl_core/IExplorerCommand::GetState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerCommand.GetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand::GetState


## -description


Gets state information associated with a specified Windows Explorer command item.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


### -param fOkToBeSlow [in]

Type: <b>BOOL</b>

<b>FALSE</b> if a verb object should not perform any memory intensive computations that could cause the UI thread to stop responding. The verb object should return E_PENDING in that case. If <b>TRUE</b>, those computations can be completed.


### -param pCmdState [out]

Type: <b><a href="https://msdn.microsoft.com/41e76b6e-9294-40b3-bb8b-bbfe487fd023">EXPCMDSTATE</a>*</b>

A pointer to a value that, when this method returns successfully, receives one or more Windows Explorer command states indicated by the <a href="https://msdn.microsoft.com/41e76b6e-9294-40b3-bb8b-bbfe487fd023">EXPCMDSTATE</a> constants.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



