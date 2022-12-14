---
UID: NF:shobjidl_core.IFileDialog.GetOptions
title: IFileDialog::GetOptions (shobjidl_core.h)
description: Gets the current flags that are set to control dialog behavior.
helpviewer_keywords: ["GetOptions","GetOptions method [Windows Shell]","GetOptions method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","GetOptions method","IFileDialog.GetOptions","IFileDialog::GetOptions","shell.IFileDialog_GetOptions","shell_IFileDialog_GetOptions","shobjidl_core/IFileDialog::GetOptions"]
old-location: shell\IFileDialog_GetOptions.htm
tech.root: shell
ms.assetid: 8a01b64d-b58e-4470-a5ed-8cf821b26c6b
ms.date: 12/05/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetOptions method, IFileDialog.GetOptions, IFileDialog::GetOptions, shell.IFileDialog_GetOptions, shell_IFileDialog_GetOptions, shobjidl_core/IFileDialog::GetOptions
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
 - IFileDialog::GetOptions
 - shobjidl_core/IFileDialog::GetOptions
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
 - IFileDialog.GetOptions
---

# IFileDialog::GetOptions


## -description

Gets the current flags that are set to control dialog behavior.

## -parameters

### -param pfos [out]

Type: <b>FILEOPENDIALOGOPTIONS*</b>

When this method returns successfully, points to a value made up of one or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions">FILEOPENDIALOGOPTIONS</a> values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

