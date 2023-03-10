---
UID: NF:propsys.IPropertyStoreFactory.GetPropertyStore
title: IPropertyStoreFactory::GetPropertyStore (propsys.h)
description: Gets an IPropertyStore object that corresponds to the supplied flags.
helpviewer_keywords: ["GetPropertyStore","GetPropertyStore method [Windows Properties]","GetPropertyStore method [Windows Properties]","IPropertyStoreFactory interface","IPropertyStoreFactory interface [Windows Properties]","GetPropertyStore method","IPropertyStoreFactory.GetPropertyStore","IPropertyStoreFactory::GetPropertyStore","_shell_IPropertyStoreFactory_GetPropertyStore","properties.IPropertyStoreFactory_GetPropertyStore","propsys/IPropertyStoreFactory::GetPropertyStore","shell.IPropertyStoreFactory_GetPropertyStore"]
old-location: properties\IPropertyStoreFactory_GetPropertyStore.htm
tech.root: properties
ms.assetid: 80cc20e1-88e2-4dee-a0fb-d75fffdfc097
ms.date: 12/05/2018
ms.keywords: GetPropertyStore, GetPropertyStore method [Windows Properties], GetPropertyStore method [Windows Properties],IPropertyStoreFactory interface, IPropertyStoreFactory interface [Windows Properties],GetPropertyStore method, IPropertyStoreFactory.GetPropertyStore, IPropertyStoreFactory::GetPropertyStore, _shell_IPropertyStoreFactory_GetPropertyStore, properties.IPropertyStoreFactory_GetPropertyStore, propsys/IPropertyStoreFactory::GetPropertyStore, shell.IPropertyStoreFactory_GetPropertyStore
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
 - IPropertyStoreFactory::GetPropertyStore
 - propsys/IPropertyStoreFactory::GetPropertyStore
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
 - IPropertyStoreFactory.GetPropertyStore
---

# IPropertyStoreFactory::GetPropertyStore


## -description

Gets an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object that corresponds to the supplied flags.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>


<a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> values that modify the store that is returned.

### -param pUnkFactory [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Optional. A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of an object that implements <a href="/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a>. If <i>pUnkFactory</i> is provided, this method can create the handler instance using <b>ICreateObject</b> rather than <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>, if implemented. The reason to provide <i>pUnkFactory</i> is usually to create the handler in a different process. However, for most users, passing <b>NULL</b> in this parameter is sufficient.

### -param riid [in]

Type: <b>REFIID</b>

A reference to IID of the object to create.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is recommended that you use the IID_PPV_ARGS macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.