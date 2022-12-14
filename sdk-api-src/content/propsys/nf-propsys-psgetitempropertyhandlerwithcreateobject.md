---
UID: NF:propsys.PSGetItemPropertyHandlerWithCreateObject
title: PSGetItemPropertyHandlerWithCreateObject function (propsys.h)
description: Retrieves a property handler for a Shell item. (PSGetItemPropertyHandlerWithCreateObject)
helpviewer_keywords: ["PSGetItemPropertyHandlerWithCreateObject","PSGetItemPropertyHandlerWithCreateObject function [Windows Properties]","_shell_PSGetItemPropertyHandlerWithCreateObject","properties.PSGetItemPropertyHandlerWithCreateObject","propsys/PSGetItemPropertyHandlerWithCreateObject","shell.PSGetItemPropertyHandlerWithCreateObject"]
old-location: properties\PSGetItemPropertyHandlerWithCreateObject.htm
tech.root: properties
ms.assetid: 82e0aa15-b67c-4c0a-bafb-f1dc5f822aec
ms.date: 12/05/2018
ms.keywords: PSGetItemPropertyHandlerWithCreateObject, PSGetItemPropertyHandlerWithCreateObject function [Windows Properties], _shell_PSGetItemPropertyHandlerWithCreateObject, properties.PSGetItemPropertyHandlerWithCreateObject, propsys/PSGetItemPropertyHandlerWithCreateObject, shell.PSGetItemPropertyHandlerWithCreateObject
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSGetItemPropertyHandlerWithCreateObject
 - propsys/PSGetItemPropertyHandlerWithCreateObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetItemPropertyHandlerWithCreateObject
---

# PSGetItemPropertyHandlerWithCreateObject function


## -description

Retrieves a property handler for a Shell item.

## -parameters

### -param punkItem [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a Shell item that supports <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

                    

<b>Windows XP:</b> Use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem">SHCreateShellItem</a> to create the Shell item.

<b>Windows Vista:</b> Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist">SHCreateItemFromIDList</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname">SHCreateItemFromParsingName</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename">SHCreateItemFromRelativeName</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder">SHCreateItemInKnownFolder</a>, or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent">SHCreateItemWithParent</a> to create the Shell item.

### -param fReadWrite [in]

Type: <b>BOOL</b>

<b>TRUE</b> to retrieve a read/write property handler. <b>FALSE</b> to retrieve a read-only property handler.

### -param punkCreateObject [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a class factory object that supports <a href="/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.

### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecapabilities">IPropertyStoreCapabilities</a>.

## -returns

Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This function is supported in Windows XP as part of the Microsoft Windows Desktop Search (WDS) redistributable which includes <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> and supporting interfaces. For applications supported only on Windows Vista or later, we recommend that you use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystorewithcreateobject">IShellItem2::GetPropertyStoreWithCreateObject</a> instead of <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandlerwithcreateobject">PSGetItemPropertyHandlerWithCreateObject</a> because <b>IShellItem2::GetPropertyStoreWithCreateObject</b> provides a richer set of properties in the property store that is returned.

This function is approximately equivalent to passing the GPS_HANDLERPROPERTIESONLY flag to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystorewithcreateobject">IShellItem2::GetPropertyStoreWithCreateObject</a>.

The <i>punkCreateObject</i> parameter enables the creation of a property store in a different context than that of the caller. For instance, the <a href="/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a> implementation can cause the property store to be created in another process. This parameter is used only for property handlers that support it and that are registered under `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\PropertySystem\PropertyHandlers`.

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before you call <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandlerwithcreateobject">PSGetItemPropertyHandlerWithCreateObject</a>. COM must remain initialized for the lifetime of this object.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandlerwithcreateobject">PSGetItemPropertyHandlerWithCreateObject</a> to obtain a property handler for an item.


```cpp
// IShellItem *psi;
// ICreateObject *pco;
// Assume variables pco and psi are valid and initialized.
IPropertyStore *pStore;

HRESULT hr = PSGetItemPropertyHandlerWithCreateObject(psi, FALSE, pco, IID_PPV_ARGS(&pStore));

if (SUCCEEDED(hr))
{
    // pStore is now valid and contains properties exposed through the 
    // property handler for the item.
 
    pStore->Release();
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystorewithcreateobject">IShellItem2::GetPropertyStoreWithCreateObject</a>



<a href="/windows/desktop/properties/building-property-handlers-property-handlers">Initializing Property Handlers</a>
