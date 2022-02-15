---
UID: NF:propsys.IDelayedPropertyStoreFactory.GetDelayedPropertyStore
title: IDelayedPropertyStoreFactory::GetDelayedPropertyStore (propsys.h)
description: Gets an IPropertyStore interface object, as specified.
helpviewer_keywords: ["GetDelayedPropertyStore","GetDelayedPropertyStore method [Windows Shell]","GetDelayedPropertyStore method [Windows Shell]","IDelayedPropertyStoreFactory interface","IDelayedPropertyStoreFactory interface [Windows Shell]","GetDelayedPropertyStore method","IDelayedPropertyStoreFactory.GetDelayedPropertyStore","IDelayedPropertyStoreFactory::GetDelayedPropertyStore","STOREID_FALLBACK","STOREID_FILE","STOREID_INNATE","_shell_IDelayedPropertyStoreFactory_GetDelayedPropertyStore","propsys/IDelayedPropertyStoreFactory::GetDelayedPropertyStore","shell.IDelayedPropertyStoreFactory_GetDelayedPropertyStore"]
old-location: shell\IDelayedPropertyStoreFactory_GetDelayedPropertyStore.htm
tech.root: shell
ms.assetid: 26df5fec-2a21-454e-9539-877c00a4f8fb
ms.date: 12/05/2018
ms.keywords: GetDelayedPropertyStore, GetDelayedPropertyStore method [Windows Shell], GetDelayedPropertyStore method [Windows Shell],IDelayedPropertyStoreFactory interface, IDelayedPropertyStoreFactory interface [Windows Shell],GetDelayedPropertyStore method, IDelayedPropertyStoreFactory.GetDelayedPropertyStore, IDelayedPropertyStoreFactory::GetDelayedPropertyStore, STOREID_FALLBACK, STOREID_FILE, STOREID_INNATE, _shell_IDelayedPropertyStoreFactory_GetDelayedPropertyStore, propsys/IDelayedPropertyStoreFactory::GetDelayedPropertyStore, shell.IDelayedPropertyStoreFactory_GetDelayedPropertyStore
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IDelayedPropertyStoreFactory::GetDelayedPropertyStore
 - propsys/IDelayedPropertyStoreFactory::GetDelayedPropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IDelayedPropertyStoreFactory.GetDelayedPropertyStore
---

# IDelayedPropertyStoreFactory::GetDelayedPropertyStore


## -description

Gets an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface object, as specified.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>

The GPS_XXX flags that modify the store that is returned. See <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a>.

### -param dwStoreId [in]

Type: <b>DWORD</b>

The property store ID. Valid values are.



#### STOREID_INNATE

Value is 0.



#### STOREID_FILE

Value is 1.



#### STOREID_FALLBACK

Value is 2.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.

### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.