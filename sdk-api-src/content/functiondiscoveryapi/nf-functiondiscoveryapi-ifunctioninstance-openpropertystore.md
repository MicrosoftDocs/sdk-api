---
UID: NF:functiondiscoveryapi.IFunctionInstance.OpenPropertyStore
title: IFunctionInstance::OpenPropertyStore (functiondiscoveryapi.h)
description: Opens the property store for the function instance.
helpviewer_keywords: ["IFunctionInstance interface","OpenPropertyStore method","IFunctionInstance.OpenPropertyStore","IFunctionInstance::OpenPropertyStore","OpenPropertyStore","OpenPropertyStore method","OpenPropertyStore method","IFunctionInstance interface","STGM_READ","STGM_READWRITE","STGM_WRITE","functiondiscoveryapi/IFunctionInstance::OpenPropertyStore","ncd.ifunctioninstance_openpropertystore_method"]
old-location: ncd\ifunctioninstance_openpropertystore_method.htm
tech.root: ncd
ms.assetid: 3e03567b-7bac-4bef-ae62-a040f0c33cfb
ms.date: 12/05/2018
ms.keywords: IFunctionInstance interface,OpenPropertyStore method, IFunctionInstance.OpenPropertyStore, IFunctionInstance::OpenPropertyStore, OpenPropertyStore, OpenPropertyStore method, OpenPropertyStore method,IFunctionInstance interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryapi/IFunctionInstance::OpenPropertyStore, ncd.ifunctioninstance_openpropertystore_method
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionInstance::OpenPropertyStore
 - functiondiscoveryapi/IFunctionInstance::OpenPropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstance.OpenPropertyStore
---

# IFunctionInstance::OpenPropertyStore


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Opens the property store for the function instance. The property store contains metadata about the function instance, such as its name, icon, installation date, and other information.

## -parameters

### -param dwStgAccess [in]

The access mode to be assigned to the open stream.  For this method, the following access modes are supported:

<a id="STGM_READ"></a>
<a id="stgm_read"></a>


#### STGM_READ

<a id="STGM_READWRITE"></a>
<a id="stgm_readwrite"></a>


#### STGM_READWRITE

<a id="STGM_WRITE"></a>
<a id="stgm_write"></a>


#### STGM_WRITE

### -param ppIPropertyStore [out]

A pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface pointer.

## -returns

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
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The method could not open a writable property store because the caller has insufficient access or the discovery provider does not allow write access to its property store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwStgAccess</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppIPropertyStore</i> points to invalid memory.

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

Only one property store per function instance can be open at a time. If <b>OpenPropertyStore</b> is called twice on the same function instance, both <i>ppIPropertyStore</i> pointers would point to the same property store. Furthermore, the access mode (as specified by the  <i>dwStgAccess</i> parameter) would be determined by the most recent <b>OpenPropertyStore</b> call. Applications should call <b>Release</b> to close a property store before opening another.

It is possible that <b>OpenPropertyStore</b> will return a property store for a device that has been removed. In this case, the property keys in the store will be empty. This situation may occur if the device's <a href="/previous-versions/windows/desktop/fundisc/function-discovery-glossary">devnode</a> was deleted but the property store associated with the device's function instance is still accessible. This situation occurs rarely.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a>