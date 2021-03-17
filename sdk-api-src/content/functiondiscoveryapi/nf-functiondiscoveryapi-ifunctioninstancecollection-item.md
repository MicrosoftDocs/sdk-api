---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Item
title: IFunctionInstanceCollection::Item (functiondiscoveryapi.h)
description: Gets the specified function instance, by index.
helpviewer_keywords: ["IFunctionInstanceCollection interface","Item method","IFunctionInstanceCollection.Item","IFunctionInstanceCollection::Item","Item","Item method","Item method","IFunctionInstanceCollection interface","functiondiscoveryapi/IFunctionInstanceCollection::Item","ncd.ifunctioninstancecollection_item_method"]
old-location: ncd\ifunctioninstancecollection_item_method.htm
tech.root: ncd
ms.assetid: b79b7cb2-c02a-4474-bd48-8907ebb118fa
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceCollection interface,Item method, IFunctionInstanceCollection.Item, IFunctionInstanceCollection::Item, Item, Item method, Item method,IFunctionInstanceCollection interface, functiondiscoveryapi/IFunctionInstanceCollection::Item, ncd.ifunctioninstancecollection_item_method
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
 - IFunctionInstanceCollection::Item
 - functiondiscoveryapi/IFunctionInstanceCollection::Item
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
 - IFunctionInstanceCollection.Item
---

# IFunctionInstanceCollection::Item


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified function instance, by index.

## -parameters

### -param dwIndex [in]

The zero-based index of the function instance to be retrieved.

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
The <i>ppFunctionInstance</i> parameter is <b>NULL</b> or <i>dwIndex</i> is out of range.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-getcount">GetCount</a> and <b>Item</b> methods enables you to enumerate all of the function instances contained in a collection using a simple <b>for</b> or <b>while</b> loop.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a>