---
UID: NF:shobjidl_core.IExecuteCommand.SetShowWindow
title: IExecuteCommand::SetShowWindow (shobjidl_core.h)
description: Sets the specified window's visual state.
helpviewer_keywords: ["IExecuteCommand interface [Windows Shell]","SetShowWindow method","IExecuteCommand.SetShowWindow","IExecuteCommand::SetShowWindow","SetShowWindow","SetShowWindow method [Windows Shell]","SetShowWindow method [Windows Shell]","IExecuteCommand interface","_shell_IExecuteCommand_SetShowWindow","shell.IExecuteCommand_SetShowWindow","shobjidl_core/IExecuteCommand::SetShowWindow"]
old-location: shell\IExecuteCommand_SetShowWindow.htm
tech.root: shell
ms.assetid: 57ac201e-0680-4856-ab05-9f8b49aecd62
ms.date: 12/05/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetShowWindow method, IExecuteCommand.SetShowWindow, IExecuteCommand::SetShowWindow, SetShowWindow, SetShowWindow method [Windows Shell], SetShowWindow method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetShowWindow, shell.IExecuteCommand_SetShowWindow, shobjidl_core/IExecuteCommand::SetShowWindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExecuteCommand::SetShowWindow
 - shobjidl_core/IExecuteCommand::SetShowWindow
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
 - IExecuteCommand.SetShowWindow
---

# IExecuteCommand::SetShowWindow


## -description

Sets the specified window's visual state.

## -parameters

### -param nShow [in]

Type: <b>int</b>

It can be any of the values that can be specified in the <i>nCmdShow</i> parameter for the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.