---
UID: NF:shobjidl_core.IFileDialog.AddPlace
title: IFileDialog::AddPlace (shobjidl_core.h)
description: Adds a folder to the list of places available for the user to open or save items.
helpviewer_keywords: ["AddPlace","AddPlace method [Windows Shell]","AddPlace method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","AddPlace method","IFileDialog.AddPlace","IFileDialog::AddPlace","shell.IFileDialog_AddPlace","shell_IFileDialog_AddPlace","shobjidl_core/IFileDialog::AddPlace"]
old-location: shell\IFileDialog_AddPlace.htm
tech.root: shell
ms.assetid: 2196e73f-4e0f-4213-b0a2-13a047486f40
ms.date: 12/05/2018
ms.keywords: AddPlace, AddPlace method [Windows Shell], AddPlace method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],AddPlace method, IFileDialog.AddPlace, IFileDialog::AddPlace, shell.IFileDialog_AddPlace, shell_IFileDialog_AddPlace, shobjidl_core/IFileDialog::AddPlace
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
 - IFileDialog::AddPlace
 - shobjidl_core/IFileDialog::AddPlace
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
 - IFileDialog.AddPlace
---

# IFileDialog::AddPlace


## -description

Adds a folder to the list of places available for the user to open or save items.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the folder to be made available to the user. This can only be a folder.

### -param fdap [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap">FDAP</a></b>

Specifies where the folder is placed within the list. See <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap">FDAP</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem">SHSetTemporaryPropertyForItem</a> can be used to set a temporary <a href="/windows/desktop/properties/props-system-itemnamedisplay">PKEY_ItemNameDisplay</a> property on the item represented by the <i>psi</i> parameter. The value for this property will be used in place of the item's UI name.