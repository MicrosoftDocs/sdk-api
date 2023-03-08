---
UID: NF:shobjidl_core.IFileSaveDialog.GetProperties
title: IFileSaveDialog::GetProperties (shobjidl_core.h)
description: Retrieves the set of property values for a saved item or an item in the process of being saved.
helpviewer_keywords: ["GetProperties","GetProperties method [Windows Shell]","GetProperties method [Windows Shell]","IFileSaveDialog interface","IFileSaveDialog interface [Windows Shell]","GetProperties method","IFileSaveDialog.GetProperties","IFileSaveDialog::GetProperties","shell.IFileSaveDialog_GetProperties","shell_IFileSaveDialog_GetProperties","shobjidl_core/IFileSaveDialog::GetProperties"]
old-location: shell\IFileSaveDialog_GetProperties.htm
tech.root: shell
ms.assetid: 734a1bf9-ff63-48a5-9508-3a576ea24ab7
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [Windows Shell], GetProperties method [Windows Shell],IFileSaveDialog interface, IFileSaveDialog interface [Windows Shell],GetProperties method, IFileSaveDialog.GetProperties, IFileSaveDialog::GetProperties, shell.IFileSaveDialog_GetProperties, shell_IFileSaveDialog_GetProperties, shobjidl_core/IFileSaveDialog::GetProperties
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
 - IFileSaveDialog::GetProperties
 - shobjidl_core/IFileSaveDialog::GetProperties
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
 - IFileSaveDialog.GetProperties
---

# IFileSaveDialog::GetProperties


## -description

Retrieves the set of property values for a saved item or an item in the process of being saved.

## -parameters

### -param ppStore [out]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> that receives the property values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be called while the dialog is showing to retrieve the current set of values in the metadata collection pane. It can also be called after the dialog has closed, to retrieve the final set of values.

The call to this method will fail unless property collection has been turned on with a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setcollectedproperties">IFileSaveDialog::SetCollectedProperties</a>.