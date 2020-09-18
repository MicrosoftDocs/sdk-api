---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Add
title: IFunctionInstanceCollection::Add (functiondiscoveryapi.h)
description: Adds a function instance to the collection.
helpviewer_keywords: ["Add","Add method","Add method","IFunctionInstanceCollection interface","IFunctionInstanceCollection interface","Add method","IFunctionInstanceCollection.Add","IFunctionInstanceCollection::Add","functiondiscoveryapi/IFunctionInstanceCollection::Add","ncd.ifunctioninstancecollection_add"]
old-location: ncd\ifunctioninstancecollection_add.htm
tech.root: ncd
ms.assetid: c77729f2-2524-4502-82d6-3a3be8344d94
ms.date: 12/05/2018
ms.keywords: Add, Add method, Add method,IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,Add method, IFunctionInstanceCollection.Add, IFunctionInstanceCollection::Add, functiondiscoveryapi/IFunctionInstanceCollection::Add, ncd.ifunctioninstancecollection_add
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
 - IFunctionInstanceCollection::Add
 - functiondiscoveryapi/IFunctionInstanceCollection::Add
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
 - IFunctionInstanceCollection.Add
---

# IFunctionInstanceCollection::Add


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Adds a function instance to the collection.

## -parameters

### -param pIFunctionInstance [in]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface for the function instance to be added to the collection.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pIFunctionInstance</i> is invalid.

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