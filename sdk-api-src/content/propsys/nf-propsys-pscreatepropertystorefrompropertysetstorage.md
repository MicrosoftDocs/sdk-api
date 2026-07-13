---
UID: NF:propsys.PSCreatePropertyStoreFromPropertySetStorage
title: PSCreatePropertyStoreFromPropertySetStorage function (propsys.h)
description: Wraps an IPropertySetStorage interface in an IPropertyStore interface.
helpviewer_keywords: ["PSCreatePropertyStoreFromPropertySetStorage","PSCreatePropertyStoreFromPropertySetStorage function [Windows Properties]","STGM_READ","STGM_READWRITE","STGM_WRITE","_shell_PSCreatePropertyStoreFromPropertySetStorage","properties.PSCreatePropertyStoreFromPropertySetStorage","propsys/PSCreatePropertyStoreFromPropertySetStorage","shell.PSCreatePropertyStoreFromPropertySetStorage"]
old-location: properties\PSCreatePropertyStoreFromPropertySetStorage.htm
tech.root: properties
ms.assetid: efba5a2a-df26-4f7e-9ddf-ec471e3d547c
ms.date: 12/05/2018
ms.keywords: PSCreatePropertyStoreFromPropertySetStorage, PSCreatePropertyStoreFromPropertySetStorage function [Windows Properties], STGM_READ, STGM_READWRITE, STGM_WRITE, _shell_PSCreatePropertyStoreFromPropertySetStorage, properties.PSCreatePropertyStoreFromPropertySetStorage, propsys/PSCreatePropertyStoreFromPropertySetStorage, shell.PSCreatePropertyStoreFromPropertySetStorage
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
 - PSCreatePropertyStoreFromPropertySetStorage
 - propsys/PSCreatePropertyStoreFromPropertySetStorage
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
 - PSCreatePropertyStoreFromPropertySetStorage
---

# PSCreatePropertyStoreFromPropertySetStorage function


## -description

Wraps an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface in an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.

## -parameters

### -param ppss [in]

Type: <b><a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>*</b>

A pointer to an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface.

### -param grfMode [in]

Type: <b>DWORD</b>

Specifies the access mode to enforce. grfMode should match the access mode used to open the <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>. Valid values are as follows:



#### STGM_READ

Calls to <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-setvalue">IPropertyStore::SetValue</a> update an internal cache of properties, and calls to <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> call the appropriate <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> methods to write out the changed properties.



#### STGM_WRITE

Not supported.



#### STGM_READWRITE

Not supported.

### -param riid [in]

Type: <b>REFIID</b>

Reference to an IID.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer specified in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function wraps an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface in an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface. Any value other than <b>STGM_READ</b> for <i>grfMode</i>, causes calls to <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-setvalue">IPropertyStore::SetValue</a> and <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> to fail with <b>STG_E_ACCESSDENIED.</b>