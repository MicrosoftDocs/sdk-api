---
UID: NF:propsys.PSGetItemPropertyHandler
title: PSGetItemPropertyHandler function (propsys.h)
description: Retrieves a property handler for a Shell item. (PSGetItemPropertyHandler)
helpviewer_keywords: ["PSGetItemPropertyHandler","PSGetItemPropertyHandler function [Windows Properties]","_shell_PSGetItemPropertyHandler","properties.PSGetItemPropertyHandler","propsys/PSGetItemPropertyHandler","shell.PSGetItemPropertyHandler"]
old-location: properties\PSGetItemPropertyHandler.htm
tech.root: properties
ms.assetid: 7b7fd260-c863-41f7-8594-4ee435090228
ms.date: 12/05/2018
ms.keywords: PSGetItemPropertyHandler, PSGetItemPropertyHandler function [Windows Properties], _shell_PSGetItemPropertyHandler, properties.PSGetItemPropertyHandler, propsys/PSGetItemPropertyHandler, shell.PSGetItemPropertyHandler
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
 - PSGetItemPropertyHandler
 - propsys/PSGetItemPropertyHandler
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
 - PSGetItemPropertyHandler
---

# PSGetItemPropertyHandler function


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

### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID of the interface the handler object should return. This should be <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or an interface derived from <b>IPropertyStore</b>.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>.

## -returns

Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This function is supported in Windows XP and Windows Vista. For applications supported only on Windows Vista or later, it is recommended that you use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a> instead of <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandler">PSGetItemPropertyHandler</a>. That method provides a richer set of properties in the property store that is returned.

This function is approximately equivalent to passing the GPS_HANDLERPROPERTIESONLY flag to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>.

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before you call <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandler">PSGetItemPropertyHandler</a>. COM must remain initialized for the lifetime of this object.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandler">PSGetItemPropertyHandler</a> to obtain a property handler for an item.


```cpp
// IShellItem *psi;
// Assume variable psi is valid and initialized.
IPropertyStore *pStore;

HRESULT hr = PSGetItemPropertyHandler(psi, FALSE, IID_PPV_ARGS(&pStore));

if (SUCCEEDED(hr))
{
    // pStore is now valid and contains properties exposed through the 
    // property handler for the item.
 
    pStore->Release();
}
```
