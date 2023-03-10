---
UID: NF:shobjidl_core.IFileDialog.SetFileTypeIndex
title: IFileDialog::SetFileTypeIndex (shobjidl_core.h)
description: Sets the file type that appears as selected in the dialog.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetFileTypeIndex method","IFileDialog.SetFileTypeIndex","IFileDialog::SetFileTypeIndex","SetFileTypeIndex","SetFileTypeIndex method [Windows Shell]","SetFileTypeIndex method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetFileTypeIndex","shell_IFileDialog_SetFileTypeIndex","shobjidl_core/IFileDialog::SetFileTypeIndex"]
old-location: shell\IFileDialog_SetFileTypeIndex.htm
tech.root: shell
ms.assetid: 733ade05-e255-4b1c-a961-e1feb749f73d
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFileTypeIndex method, IFileDialog.SetFileTypeIndex, IFileDialog::SetFileTypeIndex, SetFileTypeIndex, SetFileTypeIndex method [Windows Shell], SetFileTypeIndex method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetFileTypeIndex, shell_IFileDialog_SetFileTypeIndex, shobjidl_core/IFileDialog::SetFileTypeIndex
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
 - IFileDialog::SetFileTypeIndex
 - shobjidl_core/IFileDialog::SetFileTypeIndex
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
 - IFileDialog.SetFileTypeIndex
---

# IFileDialog::SetFileTypeIndex


## -description

Sets the file type that appears as selected in the dialog.

## -parameters

### -param iFileType [in]

Type: <b>UINT</b>

The index of the file type in the file type array passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes">IFileDialog::SetFileTypes</a> in its <i>cFileTypes</i> parameter. Note that this is a one-based index, not zero-based.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method must be called before the dialog is showing.