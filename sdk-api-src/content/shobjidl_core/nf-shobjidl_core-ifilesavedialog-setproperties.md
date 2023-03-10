---
UID: NF:shobjidl_core.IFileSaveDialog.SetProperties
title: IFileSaveDialog::SetProperties (shobjidl_core.h)
description: Provides a property store that defines the default values to be used for the item being saved.
helpviewer_keywords: ["IFileSaveDialog interface [Windows Shell]","SetProperties method","IFileSaveDialog.SetProperties","IFileSaveDialog::SetProperties","SetProperties","SetProperties method [Windows Shell]","SetProperties method [Windows Shell]","IFileSaveDialog interface","shell.IFileSaveDialog_SetProperties","shell_IFileSaveDialog_SetProperties","shobjidl_core/IFileSaveDialog::SetProperties"]
old-location: shell\IFileSaveDialog_SetProperties.htm
tech.root: shell
ms.assetid: 418f2524-5e6d-4e79-894b-b5f706171836
ms.date: 12/05/2018
ms.keywords: IFileSaveDialog interface [Windows Shell],SetProperties method, IFileSaveDialog.SetProperties, IFileSaveDialog::SetProperties, SetProperties, SetProperties method [Windows Shell], SetProperties method [Windows Shell],IFileSaveDialog interface, shell.IFileSaveDialog_SetProperties, shell_IFileSaveDialog_SetProperties, shobjidl_core/IFileSaveDialog::SetProperties
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
 - IFileSaveDialog::SetProperties
 - shobjidl_core/IFileSaveDialog::SetProperties
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
 - IFileSaveDialog.SetProperties
---

# IFileSaveDialog::SetProperties


## -description

Provides a property store that defines the default values to be used for the item being saved.

## -parameters

### -param pStore [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

Pointer to the interface that represents the property store that contains the associated metadata.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be called at any time before the dialog is opened or while the dialog is showing. If an item has inherent properties, this method should be called with those properties before showing the dialog.

When using <b>Save As</b>, the application should provide the properties of the item being saved to the <b>Save</b> dialog. Those properties should be retreived from the original item by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">GetPropertyStore</a> with the <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GPS_HANDLERPROPERTIESONLY</a> flag.

To retrieve the properties of the saved item (which may have been modified by the user) after the dialog closes, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-getproperties">IFileSaveDialog::GetProperties</a>.

To turn on property collection and indicate which properties should be displayed in the <b>Save</b> dialog, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setcollectedproperties">IFileSaveDialog::SetCollectedProperties</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesavedialog">IFileSaveDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-getproperties">IFileSaveDialog::GetProperties</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setcollectedproperties">IFileSaveDialog::SetCollectedProperties</a>