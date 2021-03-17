---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstancePropertyStoreFlush
title: IFunctionDiscoveryProvider::InstancePropertyStoreFlush (functiondiscoveryprovider.h)
description: Provides a mechanism for the provider to persist properties.
helpviewer_keywords: ["IFunctionDiscoveryProvider interface","InstancePropertyStoreFlush method","IFunctionDiscoveryProvider.InstancePropertyStoreFlush","IFunctionDiscoveryProvider::InstancePropertyStoreFlush","InstancePropertyStoreFlush","InstancePropertyStoreFlush method","InstancePropertyStoreFlush method","IFunctionDiscoveryProvider interface","functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreFlush","ncd.ifunctiondiscoveryprovider_instancepropertystoreflush"]
old-location: ncd\ifunctiondiscoveryprovider_instancepropertystoreflush.htm
tech.root: ncd
ms.assetid: 7ad29f46-fb21-4287-9fc9-9ab86d44d298
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstancePropertyStoreFlush method, IFunctionDiscoveryProvider.InstancePropertyStoreFlush, IFunctionDiscoveryProvider::InstancePropertyStoreFlush, InstancePropertyStoreFlush, InstancePropertyStoreFlush method, InstancePropertyStoreFlush method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreFlush, ncd.ifunctiondiscoveryprovider_instancepropertystoreflush
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - IFunctionDiscoveryProvider::InstancePropertyStoreFlush
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreFlush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProvider.InstancePropertyStoreFlush
---

# IFunctionDiscoveryProvider::InstancePropertyStoreFlush


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Provides a mechanism for the provider to persist properties without having to implement <a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderproperties">IProviderProperties</a>. This method is called whenever <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> is called by the client on the function instance property store.

## -parameters

### -param pIFunctionInstance [in]

 A pointer to the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.

### -param iProviderInstanceContext [in]

The context associated with the specific function instance.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The provider does not implement an instance property store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
</table>

## -remarks

If the provider keeps the new values that are passed through <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderproperties-setvalue">SetValue</a> cached in memory, this method should implement the code to persist the updated values to the underlying API/store.

If you implement this method, you should call <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">OpenPropertyStore</a> to return the current property store before persisting the data.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>