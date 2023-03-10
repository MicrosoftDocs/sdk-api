---
UID: NF:shldisp.IShellFolderViewDual.SelectedItems
title: IShellFolderViewDual::SelectedItems (shldisp.h)
description: Gets a FolderItems object that represents all of the selected items in the view.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","SelectedItems method","IShellFolderViewDual.SelectedItems","IShellFolderViewDual::SelectedItems","SelectedItems","SelectedItems method [Windows Shell]","SelectedItems method [Windows Shell]","IShellFolderViewDual interface","_shell_IShellFolderViewDual_SelectedItems","shell.IShellFolderViewDual_SelectedItems","shldisp/IShellFolderViewDual::SelectedItems"]
old-location: shell\IShellFolderViewDual_SelectedItems.htm
tech.root: shell
ms.assetid: 71ec6c0d-f3de-4a5d-941b-16d33b718921
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],SelectedItems method, IShellFolderViewDual.SelectedItems, IShellFolderViewDual::SelectedItems, SelectedItems, SelectedItems method [Windows Shell], SelectedItems method [Windows Shell],IShellFolderViewDual interface, _shell_IShellFolderViewDual_SelectedItems, shell.IShellFolderViewDual_SelectedItems, shldisp/IShellFolderViewDual::SelectedItems
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
 - IShellFolderViewDual::SelectedItems
 - shldisp/IShellFolderViewDual::SelectedItems
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
 - IShellFolderViewDual.SelectedItems
---

# IShellFolderViewDual::SelectedItems


## -description

Gets a FolderItems object that represents all of the selected items in the view.

## -parameters

### -param ppid [out]

Type: <b><a href="/windows/win32/shell/folderitem">FolderItems</a>**</b>

The FolderItems object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>