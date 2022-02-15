---
UID: NF:shobjidl_core.IExplorerCommand.GetTitle
title: IExplorerCommand::GetTitle (shobjidl_core.h)
description: Gets the title text of the button or menu item that launches a specified Windows Explorer command item.
helpviewer_keywords: ["GetTitle","GetTitle method [Windows Shell]","GetTitle method [Windows Shell]","IExplorerCommand interface","IExplorerCommand interface [Windows Shell]","GetTitle method","IExplorerCommand.GetTitle","IExplorerCommand::GetTitle","_shell_IExplorerCommand_GetTitle","shell.IExplorerCommand_GetTitle","shobjidl_core/IExplorerCommand::GetTitle"]
old-location: shell\IExplorerCommand_GetTitle.htm
tech.root: shell
ms.assetid: d03ca4c5-80a5-4b7d-a47b-a67c72b7883c
ms.date: 12/05/2018
ms.keywords: GetTitle, GetTitle method [Windows Shell], GetTitle method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetTitle method, IExplorerCommand.GetTitle, IExplorerCommand::GetTitle, _shell_IExplorerCommand_GetTitle, shell.IExplorerCommand_GetTitle, shobjidl_core/IExplorerCommand::GetTitle
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
 - IExplorerCommand::GetTitle
 - shobjidl_core/IExplorerCommand::GetTitle
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
 - IExplorerCommand.GetTitle
---

# IExplorerCommand::GetTitle


## -description

Gets the title text of the button or menu item that launches a specified Windows Explorer command item.

## -parameters

### -param psiItemArray [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

### -param ppszName [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the title string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.