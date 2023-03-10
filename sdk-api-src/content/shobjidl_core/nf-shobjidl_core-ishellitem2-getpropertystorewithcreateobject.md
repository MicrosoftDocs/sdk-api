---
UID: NF:shobjidl_core.IShellItem2.GetPropertyStoreWithCreateObject
title: IShellItem2::GetPropertyStoreWithCreateObject (shobjidl_core.h)
description: Uses the specified ICreateObject instead of CoCreateInstance to create an instance of the property handler associated with the Shell item on which this method is called.
helpviewer_keywords: ["GetPropertyStoreWithCreateObject","GetPropertyStoreWithCreateObject method [Windows Shell]","GetPropertyStoreWithCreateObject method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetPropertyStoreWithCreateObject method","IShellItem2.GetPropertyStoreWithCreateObject","IShellItem2::GetPropertyStoreWithCreateObject","_shell_IShellItem2_GetPropertyStoreWithCreateObject","shell.IShellItem2_GetPropertyStoreWithCreateObject","shobjidl_core/IShellItem2::GetPropertyStoreWithCreateObject"]
old-location: shell\IShellItem2_GetPropertyStoreWithCreateObject.htm
tech.root: shell
ms.assetid: 6a90ea62-e4d7-4876-802a-9c1f6c296714
ms.date: 12/05/2018
ms.keywords: GetPropertyStoreWithCreateObject, GetPropertyStoreWithCreateObject method [Windows Shell], GetPropertyStoreWithCreateObject method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyStoreWithCreateObject method, IShellItem2.GetPropertyStoreWithCreateObject, IShellItem2::GetPropertyStoreWithCreateObject, _shell_IShellItem2_GetPropertyStoreWithCreateObject, shell.IShellItem2_GetPropertyStoreWithCreateObject, shobjidl_core/IShellItem2::GetPropertyStoreWithCreateObject
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
 - IShellItem2::GetPropertyStoreWithCreateObject
 - shobjidl_core/IShellItem2::GetPropertyStoreWithCreateObject
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
 - IShellItem2.GetPropertyStoreWithCreateObject
---

# IShellItem2::GetPropertyStoreWithCreateObject


## -description

Uses the specified <a href="/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a> instead of <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create an instance of the property handler associated with the Shell item on which this method is called. Most calling applications do not need to call this method, and can call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a> instead.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>

The <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> constants that modify the property store object.

### -param punkCreateObject [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to a factory for low-rights creation of type <a href="/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a>.

                    

The method <a href="/windows/desktop/api/propsys/nf-propsys-icreateobject-createobject">CreateObject</a> creates an instance of a COM object. The implementation of <b>IShellItem2::GetPropertyStoreWithCreateObject</b> uses <b>CreateObject</b> instead of <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create the property handler, which is a Shell extension, for a given file type. The property handler provides many of the important properties in the property store that this method returns.

This method is useful only if the <a href="/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a> object is created in a separate process (as a LOCALSERVER instead of an INPROCSERVER), and also if this other process has lower rights than the process calling <b>IShellItem2::GetPropertyStoreWithCreateObject</b>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the object to be retrieved.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the requested <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.</div>
<div> </div>