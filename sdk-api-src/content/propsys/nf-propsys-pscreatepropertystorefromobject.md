---
UID: NF:propsys.PSCreatePropertyStoreFromObject
title: PSCreatePropertyStoreFromObject function (propsys.h)
description: Accepts the IUnknown interface of an object that supports IPropertyStore or IPropertySetStorage. If the object supports IPropertySetStorage, it is wrapped so that it supports IPropertyStore.
helpviewer_keywords: ["PSCreatePropertyStoreFromObject","PSCreatePropertyStoreFromObject function [Windows Properties]","STGM_READ","STGM_READWRITE","_shell_PSCreatePropertyStoreFromObject","properties.PSCreatePropertyStoreFromObject","propsys/PSCreatePropertyStoreFromObject","shell.PSCreatePropertyStoreFromObject"]
old-location: properties\PSCreatePropertyStoreFromObject.htm
tech.root: properties
ms.assetid: 010572d5-0357-4101-803e-0a27fc60ca5e
ms.date: 12/05/2018
ms.keywords: PSCreatePropertyStoreFromObject, PSCreatePropertyStoreFromObject function [Windows Properties], STGM_READ, STGM_READWRITE, _shell_PSCreatePropertyStoreFromObject, properties.PSCreatePropertyStoreFromObject, propsys/PSCreatePropertyStoreFromObject, shell.PSCreatePropertyStoreFromObject
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
 - PSCreatePropertyStoreFromObject
 - propsys/PSCreatePropertyStoreFromObject
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
 - PSCreatePropertyStoreFromObject
---

# PSCreatePropertyStoreFromObject function


## -description

Accepts the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of an object that supports <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>. If the object supports <b>IPropertySetStorage</b>, it is wrapped so that it supports <b>IPropertyStore</b>.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an interface that supports either <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>.

### -param grfMode [in]

Type: <b>DWORD</b>

Specifies the access mode to use. One of these values:



#### STGM_READ

Open for reading.



#### STGM_READWRITE

Open for reading and writing.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the requested IID.

### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, contains the address of a pointer to an interface guaranteed to support <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the object pointed to by <i>punk</i> already supports <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>, no wrapper is created and the <i>punk</i> is returned unaltered.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pscreatepropertystorefrompropertysetstorage">PSCreatePropertyStoreFromPropertySetStorage</a>