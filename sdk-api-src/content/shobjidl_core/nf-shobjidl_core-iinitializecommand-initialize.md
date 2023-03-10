---
UID: NF:shobjidl_core.IInitializeCommand.Initialize
title: IInitializeCommand::Initialize (shobjidl_core.h)
description: Initialize objects that share an implementation of IExplorerCommandState, IExecuteCommand or IDropTarget with the application-specified command name and its registered properties.
helpviewer_keywords: ["IInitializeCommand interface [Windows Shell]","Initialize method","IInitializeCommand.Initialize","IInitializeCommand::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeCommand interface","_shell_IInitializeCommand_Initialize","shell.IInitializeCommand_Initialize","shobjidl_core/IInitializeCommand::Initialize"]
old-location: shell\IInitializeCommand_Initialize.htm
tech.root: shell
ms.assetid: ec115bee-7ce3-428b-9081-2f21f3793de4
ms.date: 12/05/2018
ms.keywords: IInitializeCommand interface [Windows Shell],Initialize method, IInitializeCommand.Initialize, IInitializeCommand::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeCommand interface, _shell_IInitializeCommand_Initialize, shell.IInitializeCommand_Initialize, shobjidl_core/IInitializeCommand::Initialize
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
 - IInitializeCommand::Initialize
 - shobjidl_core/IInitializeCommand::Initialize
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
 - IInitializeCommand.Initialize
---

# IInitializeCommand::Initialize


## -description

Initialize objects that share an implementation of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate">IExplorerCommandState</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a> or <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> with the application-specified command name and its registered properties.

## -parameters

### -param pszCommandName [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains the command name (the name of the command key as found in the registry). For instance, if the command is registered under <b>...</b>&#92;<b>shell</b>&#92;<b>MyCommand</b>, <i>pszCommandName</i> points to "MyCommand".

### -param ppb [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

Pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> instance that can be used to read the properties related to the command in the registry. For example, a command may registry a string property under its <b>...</b>&#92;<b>shell</b>&#92;<b>MyCommand</b> subkey.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.