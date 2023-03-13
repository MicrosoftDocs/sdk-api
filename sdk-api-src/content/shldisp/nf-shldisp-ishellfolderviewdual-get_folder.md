---
UID: NF:shldisp.IShellFolderViewDual.get_Folder
title: IShellFolderViewDual::get_Folder (shldisp.h)
description: Gets the Folder object that represents the view.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","get_Folder method","IShellFolderViewDual.get_Folder","IShellFolderViewDual::get_Folder","_shell_IShellFolderViewDual_get_Folder","get_Folder","get_Folder method [Windows Shell]","get_Folder method [Windows Shell]","IShellFolderViewDual interface","shell.IShellFolderViewDual_get_Folder","shldisp/IShellFolderViewDual::get_Folder"]
old-location: shell\IShellFolderViewDual_get_Folder.htm
tech.root: shell
ms.assetid: 62af6b31-89bf-4965-a739-659f4fd932e3
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],get_Folder method, IShellFolderViewDual.get_Folder, IShellFolderViewDual::get_Folder, _shell_IShellFolderViewDual_get_Folder, get_Folder, get_Folder method [Windows Shell], get_Folder method [Windows Shell],IShellFolderViewDual interface, shell.IShellFolderViewDual_get_Folder, shldisp/IShellFolderViewDual::get_Folder
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IShellFolderViewDual::get_Folder
 - shldisp/IShellFolderViewDual::get_Folder
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
 - IShellFolderViewDual.get_Folder
---

# IShellFolderViewDual::get_Folder


## -description

Gets the Folder object that represents the view.

## -parameters

### -param ppid [out]

Type: <b><a href="/windows/win32/shell/folder">Folder</a>**</b>

The folder object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>