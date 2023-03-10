---
UID: NF:shobjidl_core.IFileDialog.GetFileName
title: IFileDialog::GetFileName (shobjidl_core.h)
description: Retrieves the text currently entered in the dialog's File name edit box.
helpviewer_keywords: ["GetFileName","GetFileName method [Windows Shell]","GetFileName method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","GetFileName method","IFileDialog.GetFileName","IFileDialog::GetFileName","shell.IFileDialog_GetFileName","shell_IFileDialog_GetFileName","shobjidl_core/IFileDialog::GetFileName"]
old-location: shell\IFileDialog_GetFileName.htm
tech.root: shell
ms.assetid: d27acb22-906a-4e5e-9239-6de3162fd263
ms.date: 12/05/2018
ms.keywords: GetFileName, GetFileName method [Windows Shell], GetFileName method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetFileName method, IFileDialog.GetFileName, IFileDialog::GetFileName, shell.IFileDialog_GetFileName, shell_IFileDialog_GetFileName, shobjidl_core/IFileDialog::GetFileName
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
 - IFileDialog::GetFileName
 - shobjidl_core/IFileDialog::GetFileName
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
 - IFileDialog.GetFileName
---

# IFileDialog::GetFileName


## -description

Retrieves the text currently entered in the dialog's <b>File name</b> edit box.

## -parameters

### -param pszName [out]

Type: <b>WCHAR**</b>

The address of a pointer to a buffer that, when this method returns successfully, receives the text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The text in the <b>File name</b> edit box does not necessarily reflect the item the user chose.  To get the item the user chose, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult">IFileDialog::GetResult</a>.

The calling application is responsible for releasing the retrieved buffer by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.