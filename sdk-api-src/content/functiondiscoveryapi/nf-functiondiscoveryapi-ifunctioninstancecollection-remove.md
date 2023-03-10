---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Remove
title: IFunctionInstanceCollection::Remove (functiondiscoveryapi.h)
description: Deletes the specified function instance and returns a pointer to the function instance being removed.
helpviewer_keywords: ["IFunctionInstanceCollection interface","Remove method","IFunctionInstanceCollection.Remove","IFunctionInstanceCollection::Remove","Remove","Remove method","Remove method","IFunctionInstanceCollection interface","functiondiscoveryapi/IFunctionInstanceCollection::Remove","ncd.ifunctioninstancecollection_remove"]
old-location: ncd\ifunctioninstancecollection_remove.htm
tech.root: ncd
ms.assetid: e5abe3e0-a07c-45e4-a590-133f6b30a7f7
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceCollection interface,Remove method, IFunctionInstanceCollection.Remove, IFunctionInstanceCollection::Remove, Remove, Remove method, Remove method,IFunctionInstanceCollection interface, functiondiscoveryapi/IFunctionInstanceCollection::Remove, ncd.ifunctioninstancecollection_remove
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
 - IFunctionInstanceCollection::Remove
 - functiondiscoveryapi/IFunctionInstanceCollection::Remove
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
 - IFunctionInstanceCollection.Remove
---

# IFunctionInstanceCollection::Remove


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes the specified function instance and returns a pointer to the function instance being removed.

## -parameters

### -param dwIndex [in]

The index number within the collection.

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