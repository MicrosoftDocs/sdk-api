---
UID: NF:shobjidl_core.IFileDialog.SetFileName
title: IFileDialog::SetFileName (shobjidl_core.h)
description: Sets the file name that appears in the File name edit box when that dialog box is opened.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetFileName method","IFileDialog.SetFileName","IFileDialog::SetFileName","SetFileName","SetFileName method [Windows Shell]","SetFileName method [Windows Shell]","IFileDialog interface","_shell_IFileDialog_SetFileName","shell.IFileDialog_SetFileName","shobjidl_core/IFileDialog::SetFileName"]
old-location: shell\IFileDialog_SetFileName.htm
tech.root: shell
ms.assetid: b8b72a76-6cdb-4675-8d84-f3c7171b8576
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFileName method, IFileDialog.SetFileName, IFileDialog::SetFileName, SetFileName, SetFileName method [Windows Shell], SetFileName method [Windows Shell],IFileDialog interface, _shell_IFileDialog_SetFileName, shell.IFileDialog_SetFileName, shobjidl_core/IFileDialog::SetFileName
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
 - IFileDialog::SetFileName
 - shobjidl_core/IFileDialog::SetFileName
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
 - IFileDialog.SetFileName
---

# IFileDialog::SetFileName


## -description

Sets the file name that appears in the <b>File name</b> edit box when that dialog box is opened.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the name of the file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

