---
UID: NF:propsys.IPropertyStoreFactory.GetPropertyStoreForKeys
title: IPropertyStoreFactory::GetPropertyStoreForKeys (propsys.h)
description: Gets an IPropertyStore object, given a set of property keys. This provides an alternative, possibly faster, method of getting an IPropertyStore object compared to calling IPropertyStoreFactory::GetPropertyStore.
helpviewer_keywords: ["GetPropertyStoreForKeys","GetPropertyStoreForKeys method [Windows Properties]","GetPropertyStoreForKeys method [Windows Properties]","IPropertyStoreFactory interface","IPropertyStoreFactory interface [Windows Properties]","GetPropertyStoreForKeys method","IPropertyStoreFactory.GetPropertyStoreForKeys","IPropertyStoreFactory::GetPropertyStoreForKeys","_shell_IPropertyStoreFactory_GetPropertyStoreForKeys","properties.IPropertyStoreFactory_GetPropertyStoreForKeys","propsys/IPropertyStoreFactory::GetPropertyStoreForKeys","shell.IPropertyStoreFactory_GetPropertyStoreForKeys"]
old-location: properties\IPropertyStoreFactory_GetPropertyStoreForKeys.htm
tech.root: properties
ms.assetid: ce17a245-46ff-412a-a807-6bc67b826c2f
ms.date: 12/05/2018
ms.keywords: GetPropertyStoreForKeys, GetPropertyStoreForKeys method [Windows Properties], GetPropertyStoreForKeys method [Windows Properties],IPropertyStoreFactory interface, IPropertyStoreFactory interface [Windows Properties],GetPropertyStoreForKeys method, IPropertyStoreFactory.GetPropertyStoreForKeys, IPropertyStoreFactory::GetPropertyStoreForKeys, _shell_IPropertyStoreFactory_GetPropertyStoreForKeys, properties.IPropertyStoreFactory_GetPropertyStoreForKeys, propsys/IPropertyStoreFactory::GetPropertyStoreForKeys, shell.IPropertyStoreFactory_GetPropertyStoreForKeys
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
 - IPropertyStoreFactory::GetPropertyStoreForKeys
 - propsys/IPropertyStoreFactory::GetPropertyStoreForKeys
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
 - IPropertyStoreFactory.GetPropertyStoreForKeys
---

# IPropertyStoreFactory::GetPropertyStoreForKeys


## -description

Gets an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object, given a set of property keys. This provides an alternative, possibly faster, method of getting an <b>IPropertyStore</b> object compared to calling <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore">IPropertyStoreFactory::GetPropertyStore</a>.

## -parameters

### -param rgKeys [in]

Type: <b>const <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures.

### -param cKeys [in]

Type: <b>UINT</b>

The number of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures in the array pointed to by <i>rgKeys</i>.

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>


<a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> values that modify the store that is returned.

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