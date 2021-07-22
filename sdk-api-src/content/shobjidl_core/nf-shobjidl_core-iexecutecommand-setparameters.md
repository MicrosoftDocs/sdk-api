---
UID: NF:shobjidl_core.IExecuteCommand.SetParameters
title: IExecuteCommand::SetParameters (shobjidl_core.h)
description: Provides parameter values for the verb.
helpviewer_keywords: ["IExecuteCommand interface [Windows Shell]","SetParameters method","IExecuteCommand.SetParameters","IExecuteCommand::SetParameters","SetParameters","SetParameters method [Windows Shell]","SetParameters method [Windows Shell]","IExecuteCommand interface","_shell_IExecuteCommand_SetParameters","shell.IExecuteCommand_SetParameters","shobjidl_core/IExecuteCommand::SetParameters"]
old-location: shell\IExecuteCommand_SetParameters.htm
tech.root: shell
ms.assetid: 3e08777c-865b-49c2-8f37-1a427c4945b4
ms.date: 12/05/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetParameters method, IExecuteCommand.SetParameters, IExecuteCommand::SetParameters, SetParameters, SetParameters method [Windows Shell], SetParameters method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetParameters, shell.IExecuteCommand_SetParameters, shobjidl_core/IExecuteCommand::SetParameters
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
 - IExecuteCommand::SetParameters
 - shobjidl_core/IExecuteCommand::SetParameters
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
 - IExecuteCommand.SetParameters
---

# IExecuteCommand::SetParameters


## -description

Provides parameter values for the verb.

## -parameters

### -param pszParameters [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains parameter values. The format and contents of this string is determined by the verb that is to be invoked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

