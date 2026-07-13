---
UID: NF:shobjidl_core.IFileDialog.GetFileTypeIndex
title: IFileDialog::GetFileTypeIndex (shobjidl_core.h)
description: Gets the currently selected file type.
helpviewer_keywords: ["GetFileTypeIndex","GetFileTypeIndex method [Windows Shell]","GetFileTypeIndex method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","GetFileTypeIndex method","IFileDialog.GetFileTypeIndex","IFileDialog::GetFileTypeIndex","shell.IFileDialog_GetFileTypeIndex","shell_IFileDialog_GetFileTypeIndex","shobjidl_core/IFileDialog::GetFileTypeIndex"]
old-location: shell\IFileDialog_GetFileTypeIndex.htm
tech.root: shell
ms.assetid: ae5b08a1-a97d-433b-88dc-938abe028384
ms.date: 12/05/2018
ms.keywords: GetFileTypeIndex, GetFileTypeIndex method [Windows Shell], GetFileTypeIndex method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetFileTypeIndex method, IFileDialog.GetFileTypeIndex, IFileDialog::GetFileTypeIndex, shell.IFileDialog_GetFileTypeIndex, shell_IFileDialog_GetFileTypeIndex, shobjidl_core/IFileDialog::GetFileTypeIndex
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
 - IFileDialog::GetFileTypeIndex
 - shobjidl_core/IFileDialog::GetFileTypeIndex
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
 - IFileDialog.GetFileTypeIndex
---

# IFileDialog::GetFileTypeIndex


## -description

Gets the currently selected file type.

## -parameters

### -param piFileType [out]

Type: <b>UINT*</b>

A pointer to a <b>UINT</b> value that receives the index of the selected file type in the file type array passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes">IFileDialog::SetFileTypes</a> in its <i>cFileTypes</i> parameter.

<div class="alert"><b>Note</b>  This is a one-based index rather than zero-based.</div>
<div> </div>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IFileDialog::GetFileTypeIndex</b> can be called either while the dialog is open or after it has closed.