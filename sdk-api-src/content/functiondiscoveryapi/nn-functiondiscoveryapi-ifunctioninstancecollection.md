---
UID: NN:functiondiscoveryapi.IFunctionInstanceCollection
title: IFunctionInstanceCollection (functiondiscoveryapi.h)
description: Represents a group of IFunctionInstance objects returned as the result of a query or get instance request.
helpviewer_keywords: ["IFunctionInstanceCollection","IFunctionInstanceCollection interface","IFunctionInstanceCollection interface","described","functiondiscoveryapi/IFunctionInstanceCollection","ncd.ifunctioninstancecollection"]
old-location: ncd\ifunctioninstancecollection.htm
tech.root: FunDisc
ms.assetid: 8ac1a406-92f3-4e39-985e-ab8fa7d28751
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceCollection, IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,described, functiondiscoveryapi/IFunctionInstanceCollection, ncd.ifunctioninstancecollection
f1_keywords:
- functiondiscoveryapi/IFunctionInstanceCollection
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FunDisc.dll
api_name:
- IFunctionInstanceCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionInstanceCollection interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface represents a group of <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> objects returned as the result of a query or get instance request through one of the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a> methods; client program do not create these collections themselves.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstanceCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionInstanceCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionInstanceCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds a function instance to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the specified function instance from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-deleteall">DeleteAll</a>
</td>
<td align="left" width="63%">
Removes all function instances from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-get">Get</a>
</td>
<td align="left" width="63%">
Gets the specified function instance and its index from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of function instances in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-item">Item</a>
</td>
<td align="left" width="63%">
Gets the specified function instance, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Deletes the specified function instance and returns a pointer to the function instance being removed.

</td>
</tr>
</table> 


## -remarks



The <b>IFunctionInstanceCollection</b> interface allows a client program to enumerate a collection of  <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> objects.



