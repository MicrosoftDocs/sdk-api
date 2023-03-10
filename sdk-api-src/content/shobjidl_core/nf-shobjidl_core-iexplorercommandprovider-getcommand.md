---
UID: NF:shobjidl_core.IExplorerCommandProvider.GetCommand
title: IExplorerCommandProvider::GetCommand (shobjidl_core.h)
description: Gets a specified Explorer command instance.
helpviewer_keywords: ["GetCommand","GetCommand method [Windows Shell]","GetCommand method [Windows Shell]","IExplorerCommandProvider interface","IExplorerCommandProvider interface [Windows Shell]","GetCommand method","IExplorerCommandProvider.GetCommand","IExplorerCommandProvider::GetCommand","_shell_IExplorerCommandProvider_GetCommand","shell.IExplorerCommandProvider_GetCommand","shobjidl_core/IExplorerCommandProvider::GetCommand"]
old-location: shell\IExplorerCommandProvider_GetCommand.htm
tech.root: shell
ms.assetid: 8ef1fb9d-03ed-4e1a-bc13-9f5caab2abb9
ms.date: 12/05/2018
ms.keywords: GetCommand, GetCommand method [Windows Shell], GetCommand method [Windows Shell],IExplorerCommandProvider interface, IExplorerCommandProvider interface [Windows Shell],GetCommand method, IExplorerCommandProvider.GetCommand, IExplorerCommandProvider::GetCommand, _shell_IExplorerCommandProvider_GetCommand, shell.IExplorerCommandProvider_GetCommand, shobjidl_core/IExplorerCommandProvider::GetCommand
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
 - IExplorerCommandProvider::GetCommand
 - shobjidl_core/IExplorerCommandProvider::GetCommand
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
 - IExplorerCommandProvider.GetCommand
---

# IExplorerCommandProvider::GetCommand


## -description

Gets a specified Explorer command instance.

## -parameters

### -param rguidCommandId

Type: <b>REFGUID</b>

A reference to a command ID as a <b>GUID</b>. Used to obtain a command definition.

### -param riid

Type: <b>REFIID</b>

A reference to the IID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid. This will typically be <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand">IExplorerCommand</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.