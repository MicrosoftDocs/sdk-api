---
UID: NF:shobjidl_core.IFileDialog.SetOptions
title: IFileDialog::SetOptions (shobjidl_core.h)
description: Sets flags to control the behavior of the dialog.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetOptions method","IFileDialog.SetOptions","IFileDialog::SetOptions","SetOptions","SetOptions method [Windows Shell]","SetOptions method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetOptions","shell_IFileDialog_SetOptions","shobjidl_core/IFileDialog::SetOptions"]
old-location: shell\IFileDialog_SetOptions.htm
tech.root: shell
ms.assetid: 99def5c2-3fc3-416c-80a6-6009927ab63e
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetOptions method, IFileDialog.SetOptions, IFileDialog::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetOptions, shell_IFileDialog_SetOptions, shobjidl_core/IFileDialog::SetOptions
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileDialog::SetOptions
 - shobjidl_core/IFileDialog::SetOptions
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
 - IFileDialog.SetOptions
---

# IFileDialog::SetOptions


## -description

Sets flags to control the behavior of the dialog.

## -parameters

### -param fos [in]

Type: <b>FILEOPENDIALOGOPTIONS</b>

One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions">FILEOPENDIALOGOPTIONS</a> values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Generally, this method should take the value that was retrieved by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions">IFileDialog::GetOptions</a> and modify it to include or exclude options by setting the appropriate flags.