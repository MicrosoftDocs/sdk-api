---
UID: NF:shldisp.IShellFolderViewDual.PopupItemMenu
title: IShellFolderViewDual::PopupItemMenu (shldisp.h)
description: Creates a shortcut menu for the specified item and returns the selected command string.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","PopupItemMenu method","IShellFolderViewDual.PopupItemMenu","IShellFolderViewDual::PopupItemMenu","PopupItemMenu","PopupItemMenu method [Windows Shell]","PopupItemMenu method [Windows Shell]","IShellFolderViewDual interface","_shell_IShellFolderViewDual_PopupItemMenu","shell.IShellFolderViewDual_PopupItemMenu","shldisp/IShellFolderViewDual::PopupItemMenu"]
old-location: shell\IShellFolderViewDual_PopupItemMenu.htm
tech.root: shell
ms.assetid: f44e91b7-b651-4b6f-9583-cd9335ae6369
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],PopupItemMenu method, IShellFolderViewDual.PopupItemMenu, IShellFolderViewDual::PopupItemMenu, PopupItemMenu, PopupItemMenu method [Windows Shell], PopupItemMenu method [Windows Shell],IShellFolderViewDual interface, _shell_IShellFolderViewDual_PopupItemMenu, shell.IShellFolderViewDual_PopupItemMenu, shldisp/IShellFolderViewDual::PopupItemMenu
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
 - IShellFolderViewDual::PopupItemMenu
 - shldisp/IShellFolderViewDual::PopupItemMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual.PopupItemMenu
---

# IShellFolderViewDual::PopupItemMenu


## -description

Creates a shortcut menu for the specified item and returns the selected command string.

## -parameters

### -param pfi [in, optional]

Type: <b><a href="/windows/win32/shell/folderitem">FolderItem</a>*</b>

The FolderItem for which to create a shortcut menu.

### -param vx [in, optional]

Type: <b>VARIANT</b>

Optional.

### -param vy [in, optional]

Type: <b>VARIANT</b>

Optional.

### -param pbs [out]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>*</b>

The command string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>