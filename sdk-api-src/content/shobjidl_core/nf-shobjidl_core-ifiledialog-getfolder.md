---
UID: NF:shobjidl_core.IFileDialog.GetFolder
title: IFileDialog::GetFolder (shobjidl_core.h)
description: Gets either the folder currently selected in the dialog, or, if the dialog is not currently displayed, the folder that is to be selected when the dialog is opened.
helpviewer_keywords: ["GetFolder","GetFolder method [Windows Shell]","GetFolder method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","GetFolder method","IFileDialog.GetFolder","IFileDialog::GetFolder","shell.IFileDialog_GetFolder","shell_IFileDialog_GetFolder","shobjidl_core/IFileDialog::GetFolder"]
old-location: shell\IFileDialog_GetFolder.htm
tech.root: shell
ms.assetid: 424d1507-e42a-43d7-8904-347bfb311dd4
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Windows Shell], GetFolder method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetFolder method, IFileDialog.GetFolder, IFileDialog::GetFolder, shell.IFileDialog_GetFolder, shell_IFileDialog_GetFolder, shobjidl_core/IFileDialog::GetFolder
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
 - IFileDialog::GetFolder
 - shobjidl_core/IFileDialog::GetFolder
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
 - IFileDialog.GetFolder
---

# IFileDialog::GetFolder


## -description

Gets either the folder currently selected in the dialog, or, if the dialog is not currently displayed, the folder that is to be selected when the dialog is opened.

## -parameters

### -param ppsi [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The address of a pointer to the interface that represents the folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The calling application is responsible for releasing the retrieved <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> when it is no longer needed.