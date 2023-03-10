---
UID: NF:shobjidl_core.IExplorerCommand.GetCanonicalName
title: IExplorerCommand::GetCanonicalName (shobjidl_core.h)
description: Gets the GUID of a Windows Explorer command.
helpviewer_keywords: ["GetCanonicalName","GetCanonicalName method [Windows Shell]","GetCanonicalName method [Windows Shell]","IExplorerCommand interface","IExplorerCommand interface [Windows Shell]","GetCanonicalName method","IExplorerCommand.GetCanonicalName","IExplorerCommand::GetCanonicalName","_shell_IExplorerCommand_GetCanonicalName","shell.IExplorerCommand_GetCanonicalName","shobjidl_core/IExplorerCommand::GetCanonicalName"]
old-location: shell\IExplorerCommand_GetCanonicalName.htm
tech.root: shell
ms.assetid: c0f2fc66-98f5-404f-9d82-0290ed235ac0
ms.date: 12/05/2018
ms.keywords: GetCanonicalName, GetCanonicalName method [Windows Shell], GetCanonicalName method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetCanonicalName method, IExplorerCommand.GetCanonicalName, IExplorerCommand::GetCanonicalName, _shell_IExplorerCommand_GetCanonicalName, shell.IExplorerCommand_GetCanonicalName, shobjidl_core/IExplorerCommand::GetCanonicalName
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
 - IExplorerCommand::GetCanonicalName
 - shobjidl_core/IExplorerCommand::GetCanonicalName
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
 - IExplorerCommand.GetCanonicalName
---

# IExplorerCommand::GetCanonicalName


## -description

Gets the GUID of a Windows Explorer command.

## -parameters

### -param pguidCommandName [out]

Type: <b>GUID*</b>

A pointer to a value that, when this method returns successfully, receives the command's GUID, under which it is declared in the registry.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is somewhat misnamed, given that it retrieves a GUID. To retrieve the command's canonical name, you must take the additional step to pull it from the command's subkey. The GUID is the name of the subkey. where that information is stored.

