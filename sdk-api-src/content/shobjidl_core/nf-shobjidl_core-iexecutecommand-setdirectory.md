---
UID: NF:shobjidl_core.IExecuteCommand.SetDirectory
title: IExecuteCommand::SetDirectory (shobjidl_core.h)
description: Sets a new working directory.
helpviewer_keywords: ["IExecuteCommand interface [Windows Shell]","SetDirectory method","IExecuteCommand.SetDirectory","IExecuteCommand::SetDirectory","SetDirectory","SetDirectory method [Windows Shell]","SetDirectory method [Windows Shell]","IExecuteCommand interface","_shell_IExecuteCommand_SetDirectory","shell.IExecuteCommand_SetDirectory","shobjidl_core/IExecuteCommand::SetDirectory"]
old-location: shell\IExecuteCommand_SetDirectory.htm
tech.root: shell
ms.assetid: 8416b2ef-8e62-4679-adc1-ec953875db34
ms.date: 12/05/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetDirectory method, IExecuteCommand.SetDirectory, IExecuteCommand::SetDirectory, SetDirectory, SetDirectory method [Windows Shell], SetDirectory method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetDirectory, shell.IExecuteCommand_SetDirectory, shobjidl_core/IExecuteCommand::SetDirectory
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
 - IExecuteCommand::SetDirectory
 - shobjidl_core/IExecuteCommand::SetDirectory
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
 - IExecuteCommand.SetDirectory
---

# IExecuteCommand::SetDirectory


## -description

Sets a new working directory.

## -parameters

### -param pszDirectory [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated string with the fully qualified path of the new working directory. If this value is <b>NULL</b>, the current working directory is used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

