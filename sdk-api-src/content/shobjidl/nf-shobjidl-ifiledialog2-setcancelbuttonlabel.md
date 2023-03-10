---
UID: NF:shobjidl.IFileDialog2.SetCancelButtonLabel
title: IFileDialog2::SetCancelButtonLabel (shobjidl.h)
description: Replaces the default text &quot;Cancel&quot; on the common file dialog's Cancel button.
helpviewer_keywords: ["IFileDialog2 interface [Windows Shell]","SetCancelButtonLabel method","IFileDialog2.SetCancelButtonLabel","IFileDialog2::SetCancelButtonLabel","SetCancelButtonLabel","SetCancelButtonLabel method [Windows Shell]","SetCancelButtonLabel method [Windows Shell]","IFileDialog2 interface","_shell_IFileDialog2_SetCancelButtonLabel","shell.IFileDialog2_SetCancelButtonLabel","shobjidl/IFileDialog2::SetCancelButtonLabel"]
old-location: shell\IFileDialog2_SetCancelButtonLabel.htm
tech.root: shell
ms.assetid: a0d7b516-1941-4245-8ca6-f470b8c426aa
ms.date: 12/05/2018
ms.keywords: IFileDialog2 interface [Windows Shell],SetCancelButtonLabel method, IFileDialog2.SetCancelButtonLabel, IFileDialog2::SetCancelButtonLabel, SetCancelButtonLabel, SetCancelButtonLabel method [Windows Shell], SetCancelButtonLabel method [Windows Shell],IFileDialog2 interface, _shell_IFileDialog2_SetCancelButtonLabel, shell.IFileDialog2_SetCancelButtonLabel, shobjidl/IFileDialog2::SetCancelButtonLabel
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileDialog2::SetCancelButtonLabel
 - shobjidl/IFileDialog2::SetCancelButtonLabel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IFileDialog2.SetCancelButtonLabel
---

# IFileDialog2::SetCancelButtonLabel


## -description

Replaces the default text "Cancel" on the common file dialog's <b>Cancel</b> button.

## -parameters

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains the new text to display on the button.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Changing the text on the Cancel button can be useful for situations where the IFileDialogEvents::OnFileOk method is used to accumulate items, and the button text should be Done instead of Cancel, for example.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-ifiledialog2">IFileDialog2</a>