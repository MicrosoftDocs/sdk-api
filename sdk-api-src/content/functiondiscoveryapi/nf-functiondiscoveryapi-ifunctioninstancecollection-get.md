---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Get
title: IFunctionInstanceCollection::Get (functiondiscoveryapi.h)
description: Gets the specified function instance and its index from the collection.
helpviewer_keywords: ["Get","Get method","Get method","IFunctionInstanceCollection interface","IFunctionInstanceCollection interface","Get method","IFunctionInstanceCollection.Get","IFunctionInstanceCollection::Get","functiondiscoveryapi/IFunctionInstanceCollection::Get","ncd.ifunctioninstancecollection_get"]
old-location: ncd\ifunctioninstancecollection_get.htm
tech.root: ncd
ms.assetid: 3f3db880-a765-4a18-91ac-d091728cbb39
ms.date: 12/05/2018
ms.keywords: Get, Get method, Get method,IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,Get method, IFunctionInstanceCollection.Get, IFunctionInstanceCollection::Get, functiondiscoveryapi/IFunctionInstanceCollection::Get, ncd.ifunctioninstancecollection_get
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
 - IFunctionInstanceCollection::Get
 - functiondiscoveryapi/IFunctionInstanceCollection::Get
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
 - IFunctionInstanceCollection.Get
---

# IFunctionInstanceCollection::Get


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified function instance and its index from the collection.

## -parameters

### -param pszInstanceIdentity [in]

The identifier of the function instance to be retrieved (see <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getid">GetID</a>).

### -param pdwIndex [out]

The index number.

### -param ppIFunctionInstance [out]

 A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface pointer that receives the function instance.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function instance identified by <i>pInstanceIdentity</i> is not present in the function instance collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pdwIndex</i> or <i>pInstanceIdentity</i> is invalid.

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

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a>