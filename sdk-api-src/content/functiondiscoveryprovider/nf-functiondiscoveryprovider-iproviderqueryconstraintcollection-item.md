---
UID: NF:functiondiscoveryprovider.IProviderQueryConstraintCollection.Item
title: IProviderQueryConstraintCollection::Item (functiondiscoveryprovider.h)
description: Gets the name and value of the specified query constraint, by index.
helpviewer_keywords: ["IProviderQueryConstraintCollection interface","Item method","IProviderQueryConstraintCollection.Item","IProviderQueryConstraintCollection::Item","Item","Item method","Item method","IProviderQueryConstraintCollection interface","functiondiscoveryprovider/IProviderQueryConstraintCollection::Item","ncd.iproviderqueryconstraintcollection_item"]
old-location: ncd\iproviderqueryconstraintcollection_item.htm
tech.root: ncd
ms.assetid: db8840db-365a-485d-9097-ef98a9d875bc
ms.date: 12/05/2018
ms.keywords: IProviderQueryConstraintCollection interface,Item method, IProviderQueryConstraintCollection.Item, IProviderQueryConstraintCollection::Item, Item, Item method, Item method,IProviderQueryConstraintCollection interface, functiondiscoveryprovider/IProviderQueryConstraintCollection::Item, ncd.iproviderqueryconstraintcollection_item
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
 - IProviderQueryConstraintCollection::Item
 - functiondiscoveryprovider/IProviderQueryConstraintCollection::Item
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
 - IProviderQueryConstraintCollection.Item
---

# IProviderQueryConstraintCollection::Item


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the name and value of the specified query constraint, by index.

## -parameters

### -param dwIndex [in]

The index of the item in the collection.

### -param ppszConstraintName [out]

The constraint name.

### -param ppszConstraintValue [out]

The constraint value.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszConstraintName</i> or <i>ppszConstraintValue</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderqueryconstraintcollection">IProviderQueryConstraintCollection</a>