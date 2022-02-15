---
UID: NF:shobjidl_core.IFileDialog.Unadvise
title: IFileDialog::Unadvise (shobjidl_core.h)
description: Removes an event handler that was attached through the IFileDialog::Advise method.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","Unadvise method","IFileDialog.Unadvise","IFileDialog::Unadvise","Unadvise","Unadvise method [Windows Shell]","Unadvise method [Windows Shell]","IFileDialog interface","shell.IFileDialog_Unadvise","shell_IFileDialog_Unadvise","shobjidl_core/IFileDialog::Unadvise"]
old-location: shell\IFileDialog_Unadvise.htm
tech.root: shell
ms.assetid: 48504141-6612-43fe-8470-a9871b560f1a
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],Unadvise method, IFileDialog.Unadvise, IFileDialog::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IFileDialog interface, shell.IFileDialog_Unadvise, shell_IFileDialog_Unadvise, shobjidl_core/IFileDialog::Unadvise
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
 - IFileDialog::Unadvise
 - shobjidl_core/IFileDialog::Unadvise
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
 - IFileDialog.Unadvise
---

# IFileDialog::Unadvise


## -description

Removes an event handler that was attached through the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise">IFileDialog::Advise</a> method.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

The <b>DWORD</b> value that represents the event handler. This value is obtained through the <i>pdwCookie</i> parameter of the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise">IFileDialog::Advise</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.