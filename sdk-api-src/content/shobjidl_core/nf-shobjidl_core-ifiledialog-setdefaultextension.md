---
UID: NF:shobjidl_core.IFileDialog.SetDefaultExtension
title: IFileDialog::SetDefaultExtension (shobjidl_core.h)
description: Sets the default extension to be added to file names.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetDefaultExtension method","IFileDialog.SetDefaultExtension","IFileDialog::SetDefaultExtension","SetDefaultExtension","SetDefaultExtension method [Windows Shell]","SetDefaultExtension method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetDefaultExtension","shell_IFileDialog_SetDefaultExtension","shobjidl_core/IFileDialog::SetDefaultExtension"]
old-location: shell\IFileDialog_SetDefaultExtension.htm
tech.root: shell
ms.assetid: 2e1739f4-d229-4bf1-99f4-6bded830de2b
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetDefaultExtension method, IFileDialog.SetDefaultExtension, IFileDialog::SetDefaultExtension, SetDefaultExtension, SetDefaultExtension method [Windows Shell], SetDefaultExtension method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetDefaultExtension, shell_IFileDialog_SetDefaultExtension, shobjidl_core/IFileDialog::SetDefaultExtension
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
 - IFileDialog::SetDefaultExtension
 - shobjidl_core/IFileDialog::SetDefaultExtension
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
 - IFileDialog.SetDefaultExtension
---

# IFileDialog::SetDefaultExtension


## -description

Sets the default extension to be added to file names.

## -parameters

### -param pszDefaultExtension [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the extension text. This string should not include a leading period. For example, "jpg" is correct, while ".jpg" is not.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method is called before showing the dialog, the dialog will update the default extension automatically when the user chooses a new file type (see <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes">SetFileTypes</a>).