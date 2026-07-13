---
UID: NF:shobjidl_core.IFileSaveDialog.ApplyProperties
title: IFileSaveDialog::ApplyProperties (shobjidl_core.h)
description: Applies a set of properties to an item using the Shell's copy engine.
helpviewer_keywords: ["ApplyProperties","ApplyProperties method [Windows Shell]","ApplyProperties method [Windows Shell]","IFileSaveDialog interface","IFileSaveDialog interface [Windows Shell]","ApplyProperties method","IFileSaveDialog.ApplyProperties","IFileSaveDialog::ApplyProperties","shell.IFileSaveDialog_ApplyProperties","shell_IFileSaveDialog_ApplyProperties","shobjidl_core/IFileSaveDialog::ApplyProperties"]
old-location: shell\IFileSaveDialog_ApplyProperties.htm
tech.root: shell
ms.assetid: 3de64914-b64e-47e8-8f84-6c64d849ffa9
ms.date: 12/05/2018
ms.keywords: ApplyProperties, ApplyProperties method [Windows Shell], ApplyProperties method [Windows Shell],IFileSaveDialog interface, IFileSaveDialog interface [Windows Shell],ApplyProperties method, IFileSaveDialog.ApplyProperties, IFileSaveDialog::ApplyProperties, shell.IFileSaveDialog_ApplyProperties, shell_IFileSaveDialog_ApplyProperties, shobjidl_core/IFileSaveDialog::ApplyProperties
req.header: shobjidl_core.h
req.include-header: 
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
 - IFileSaveDialog::ApplyProperties
 - shobjidl_core/IFileSaveDialog::ApplyProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog.ApplyProperties
---

# IFileSaveDialog::ApplyProperties


## -description

Applies a set of properties to an item using the Shell's copy engine.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the file being saved. This is usually the item retrieved by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult">GetResult</a>.

### -param pStore [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

Pointer to the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> that represents the property values to be applied to the file. This can be the property store returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-getproperties">IFileSaveDialog::GetProperties</a>.

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the application window.

### -param pSink [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an optional <b>IFileOperationProgressSink</b> that the calling application can use if they want to be notified of the progress of the property stamping. This value may be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should be used when the application has turned on property collection (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setcollectedproperties">IFileSaveDialog::SetCollectedProperties</a>), but does not persist the properties themselves into the saved file.

<div class="alert"><b>Note</b>  The file represented by the item specified in <i>psi</i> must exist in physical storage before making the call to <b>IFileSaveDialog::ApplyProperties</b>, so it must have been previously saved at some point.</div>
<div> </div>