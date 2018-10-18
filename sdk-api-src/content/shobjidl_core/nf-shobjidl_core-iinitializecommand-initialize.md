---
UID: NF:shobjidl_core.IInitializeCommand.Initialize
title: IInitializeCommand::Initialize
author: windows-sdk-content
description: Initialize objects that share an implementation of IExplorerCommandState, IExecuteCommand or IDropTarget with the application-specified command name and its registered properties.
old-location: shell\IInitializeCommand_Initialize.htm
tech.root: shell
ms.assetid: ec115bee-7ce3-428b-9081-2f21f3793de4
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IInitializeCommand interface [Windows Shell],Initialize method, IInitializeCommand.Initialize, IInitializeCommand::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeCommand interface, _shell_IInitializeCommand_Initialize, shell.IInitializeCommand_Initialize, shobjidl_core/IInitializeCommand::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInitializeCommand.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInitializeCommand::Initialize


## -description


Initialize objects that share an implementation of <a href="https://msdn.microsoft.com/020a6f6f-1d45-44bd-a57f-ef8000976b5b">IExplorerCommandState</a>, <a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a> or <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> with the application-specified command name and its registered properties.


## -parameters




### -param pszCommandName [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains the command name (the name of the command key as found in the registry). For instance, if the command is registered under <b>...</b>\<b>shell</b>\<b>MyCommand</b>, <i>pszCommandName</i> points to "MyCommand".


### -param ppb [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> instance that can be used to read the properties related to the command in the registry. For example, a command may registry a string property under its <b>...</b>\<b>shell</b>\<b>MyCommand</b> subkey.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



