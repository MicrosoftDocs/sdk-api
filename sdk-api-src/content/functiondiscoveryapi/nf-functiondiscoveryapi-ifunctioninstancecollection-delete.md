---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Delete
title: IFunctionInstanceCollection::Delete (functiondiscoveryapi.h)
description: Removes the specified function instance from the collection.
helpviewer_keywords: ["Delete","Delete method","Delete method","IFunctionInstanceCollection interface","IFunctionInstanceCollection interface","Delete method","IFunctionInstanceCollection.Delete","IFunctionInstanceCollection::Delete","functiondiscoveryapi/IFunctionInstanceCollection::Delete","ncd.ifunctioninstancecollection_delete"]
old-location: ncd\ifunctioninstancecollection_delete.htm
tech.root: ncd
ms.assetid: e7f94912-9656-4a6b-8754-eb37358b5f9d
ms.date: 12/05/2018
ms.keywords: Delete, Delete method, Delete method,IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,Delete method, IFunctionInstanceCollection.Delete, IFunctionInstanceCollection::Delete, functiondiscoveryapi/IFunctionInstanceCollection::Delete, ncd.ifunctioninstancecollection_delete
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
 - IFunctionInstanceCollection::Delete
 - functiondiscoveryapi/IFunctionInstanceCollection::Delete
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
 - IFunctionInstanceCollection.Delete
---

# IFunctionInstanceCollection::Delete


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes the specified function instance from the collection.

## -parameters

### -param dwIndex [in]

The index number of the item to be removed from the collection.

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
The value of <i>dwIndex</i> is invalid.

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