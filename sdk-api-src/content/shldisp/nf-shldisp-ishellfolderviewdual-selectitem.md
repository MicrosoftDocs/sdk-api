---
UID: NF:shldisp.IShellFolderViewDual.SelectItem
title: IShellFolderViewDual::SelectItem (shldisp.h)
description: Sets the selection state of an item in the view.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","SelectItem method","IShellFolderViewDual.SelectItem","IShellFolderViewDual::SelectItem","SelectItem","SelectItem method [Windows Shell]","SelectItem method [Windows Shell]","IShellFolderViewDual interface","_shell_IShellFolderViewDual_SelectItem","shell.IShellFolderViewDual_SelectItem","shldisp/IShellFolderViewDual::SelectItem"]
old-location: shell\IShellFolderViewDual_SelectItem.htm
tech.root: shell
ms.assetid: fb9bc12f-bf5f-42f2-a1cd-160298f7c73a
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],SelectItem method, IShellFolderViewDual.SelectItem, IShellFolderViewDual::SelectItem, SelectItem, SelectItem method [Windows Shell], SelectItem method [Windows Shell],IShellFolderViewDual interface, _shell_IShellFolderViewDual_SelectItem, shell.IShellFolderViewDual_SelectItem, shldisp/IShellFolderViewDual::SelectItem
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
 - IShellFolderViewDual::SelectItem
 - shldisp/IShellFolderViewDual::SelectItem
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
 - IShellFolderViewDual.SelectItem
---

# IShellFolderViewDual::SelectItem


## -description

Sets the selection state of an item in the view.

## -parameters

### -param pvfi [in]

Type: <b>VARIANT*</b>

A VARIANT object.

### -param dwFlags [in]

Type: <b>int</b>

The flags representing the state of the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>