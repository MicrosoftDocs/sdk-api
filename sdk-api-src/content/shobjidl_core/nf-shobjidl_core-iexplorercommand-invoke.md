---
UID: NF:shobjidl_core.IExplorerCommand.Invoke
title: IExplorerCommand::Invoke (shobjidl_core.h)
description: Invokes a Windows Explorer command.
helpviewer_keywords: ["IExplorerCommand interface [Windows Shell]","Invoke method","IExplorerCommand.Invoke","IExplorerCommand::Invoke","Invoke","Invoke method [Windows Shell]","Invoke method [Windows Shell]","IExplorerCommand interface","_shell_IExplorerCommand_Invoke","shell.IExplorerCommand_Invoke","shobjidl_core/IExplorerCommand::Invoke"]
old-location: shell\IExplorerCommand_Invoke.htm
tech.root: shell
ms.assetid: 3ea545a4-5f4c-4f98-9e56-b7c7eed5f821
ms.date: 12/05/2018
ms.keywords: IExplorerCommand interface [Windows Shell],Invoke method, IExplorerCommand.Invoke, IExplorerCommand::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],IExplorerCommand interface, _shell_IExplorerCommand_Invoke, shell.IExplorerCommand_Invoke, shobjidl_core/IExplorerCommand::Invoke
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
 - IExplorerCommand::Invoke
 - shobjidl_core/IExplorerCommand::Invoke
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
 - IExplorerCommand.Invoke
---

# IExplorerCommand::Invoke


## -description

Invokes a Windows Explorer command.

## -parameters

### -param psiItemArray [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface, which provides access to a bind context. This value can be <b>NULL</b> if no bind context is needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.