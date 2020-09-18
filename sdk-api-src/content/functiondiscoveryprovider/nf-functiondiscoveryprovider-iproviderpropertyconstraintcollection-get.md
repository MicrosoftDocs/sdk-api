---
UID: NF:functiondiscoveryprovider.IProviderPropertyConstraintCollection.Get
title: IProviderPropertyConstraintCollection::Get (functiondiscoveryprovider.h)
description: Gets the name and value of the specified property constraint, by property key.
helpviewer_keywords: ["Get","Get method","Get method","IProviderPropertyConstraintCollection interface","IProviderPropertyConstraintCollection interface","Get method","IProviderPropertyConstraintCollection.Get","IProviderPropertyConstraintCollection::Get","functiondiscoveryprovider/IProviderPropertyConstraintCollection::Get","ncd.iproviderpropertyconstraintcollection_get"]
old-location: ncd\iproviderpropertyconstraintcollection_get.htm
tech.root: ncd
ms.assetid: 0388d895-07bb-490c-9fce-0821a51d765a
ms.date: 12/05/2018
ms.keywords: Get, Get method, Get method,IProviderPropertyConstraintCollection interface, IProviderPropertyConstraintCollection interface,Get method, IProviderPropertyConstraintCollection.Get, IProviderPropertyConstraintCollection::Get, functiondiscoveryprovider/IProviderPropertyConstraintCollection::Get, ncd.iproviderpropertyconstraintcollection_get
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
 - IProviderPropertyConstraintCollection::Get
 - functiondiscoveryprovider/IProviderPropertyConstraintCollection::Get
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
 - IProviderPropertyConstraintCollection.Get
---

# IProviderPropertyConstraintCollection::Get


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the name and value of the specified property constraint, by property key.

## -parameters

### -param Key [in]

The property key.

### -param pPropVar [out]

A <b>VARIANT</b> used for the property key constraint value.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully, but the property key was not found in the collection.

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