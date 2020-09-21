---
UID: NF:functiondiscoveryprovider.IProviderPropertyConstraintCollection.Item
title: IProviderPropertyConstraintCollection::Item (functiondiscoveryprovider.h)
description: Gets the name and value of the specified property constraint, by index.
helpviewer_keywords: ["IProviderPropertyConstraintCollection interface","Item method","IProviderPropertyConstraintCollection.Item","IProviderPropertyConstraintCollection::Item","Item","Item method","Item method","IProviderPropertyConstraintCollection interface","functiondiscoveryprovider/IProviderPropertyConstraintCollection::Item","ncd.iproviderpropertyconstraintcollection_item"]
old-location: ncd\iproviderpropertyconstraintcollection_item.htm
tech.root: ncd
ms.assetid: 3e5643f6-02a5-48b0-a105-5b82c439b5cc
ms.date: 12/05/2018
ms.keywords: IProviderPropertyConstraintCollection interface,Item method, IProviderPropertyConstraintCollection.Item, IProviderPropertyConstraintCollection::Item, Item, Item method, Item method,IProviderPropertyConstraintCollection interface, functiondiscoveryprovider/IProviderPropertyConstraintCollection::Item, ncd.iproviderpropertyconstraintcollection_item
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
 - IProviderPropertyConstraintCollection::Item
 - functiondiscoveryprovider/IProviderPropertyConstraintCollection::Item
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
 - IProviderPropertyConstraintCollection.Item
---

# IProviderPropertyConstraintCollection::Item


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the name and value of the specified property constraint, by index.

## -parameters

### -param dwIndex [in]

The index of the item in the collection.

### -param pKey [out]

The property key.

### -param pPropVar [out]

A <b>PROPVARIANT</b> used for the property constraint data.

### -param pdwPropertyConstraint [out]

The type of constraint to apply.

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
The <i>ppropVar</i> or <i>pdwPropertyConstraint</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderpropertyconstraintcollection">IProviderPropertyConstraintCollection</a>