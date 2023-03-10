---
UID: NF:shldisp.IShellFolderViewDual.get_FocusedItem
title: IShellFolderViewDual::get_FocusedItem (shldisp.h)
description: Gets the FolderItem object that represents the item that has input focus.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","get_FocusedItem method","IShellFolderViewDual.get_FocusedItem","IShellFolderViewDual::get_FocusedItem","_shell_IShellFolderViewDual_get_FocusedItem","get_FocusedItem","get_FocusedItem method [Windows Shell]","get_FocusedItem method [Windows Shell]","IShellFolderViewDual interface","shell.IShellFolderViewDual_get_FocusedItem","shldisp/IShellFolderViewDual::get_FocusedItem"]
old-location: shell\IShellFolderViewDual_get_FocusedItem.htm
tech.root: shell
ms.assetid: e3e70cbe-51df-4749-8c6c-f3a43b33c436
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],get_FocusedItem method, IShellFolderViewDual.get_FocusedItem, IShellFolderViewDual::get_FocusedItem, _shell_IShellFolderViewDual_get_FocusedItem, get_FocusedItem, get_FocusedItem method [Windows Shell], get_FocusedItem method [Windows Shell],IShellFolderViewDual interface, shell.IShellFolderViewDual_get_FocusedItem, shldisp/IShellFolderViewDual::get_FocusedItem
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
 - IShellFolderViewDual::get_FocusedItem
 - shldisp/IShellFolderViewDual::get_FocusedItem
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
 - IShellFolderViewDual.get_FocusedItem
---

# IShellFolderViewDual::get_FocusedItem


## -description

Gets the FolderItem object that represents the item that has input focus.

## -parameters

### -param ppid [out]

Type: <b><a href="/windows/win32/shell/folderitem">FolderItem</a>**</b>

The FolderItem object with input focus.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>