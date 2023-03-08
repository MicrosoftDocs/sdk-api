---
UID: NF:shobjidl_core.IExplorerCommand.GetIcon
title: IExplorerCommand::GetIcon (shobjidl_core.h)
description: Gets an icon resource string of the icon associated with the specified Windows Explorer command item.
helpviewer_keywords: ["GetIcon","GetIcon method [Windows Shell]","GetIcon method [Windows Shell]","IExplorerCommand interface","IExplorerCommand interface [Windows Shell]","GetIcon method","IExplorerCommand.GetIcon","IExplorerCommand::GetIcon","_shell_IExplorerCommand_GetIcon","shell.IExplorerCommand_GetIcon","shobjidl_core/IExplorerCommand::GetIcon"]
old-location: shell\IExplorerCommand_GetIcon.htm
tech.root: shell
ms.assetid: e71b6748-84fc-4944-90b8-a5b0bf97079d
ms.date: 12/05/2018
ms.keywords: GetIcon, GetIcon method [Windows Shell], GetIcon method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetIcon method, IExplorerCommand.GetIcon, IExplorerCommand::GetIcon, _shell_IExplorerCommand_GetIcon, shell.IExplorerCommand_GetIcon, shobjidl_core/IExplorerCommand::GetIcon
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
 - IExplorerCommand::GetIcon
 - shobjidl_core/IExplorerCommand::GetIcon
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
 - IExplorerCommand.GetIcon
---

# IExplorerCommand::GetIcon


## -description

Gets an icon resource string of the icon associated with the specified Windows Explorer command item.

## -parameters

### -param psiItemArray [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

### -param ppszIcon [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the resource string that identifies the icon source.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The retrieved icon resource string is in the standard format, for instance "shell32.dll,-249".