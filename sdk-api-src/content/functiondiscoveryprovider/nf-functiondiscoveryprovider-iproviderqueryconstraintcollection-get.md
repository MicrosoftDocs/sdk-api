---
UID: NF:functiondiscoveryprovider.IProviderQueryConstraintCollection.Get
title: IProviderQueryConstraintCollection::Get (functiondiscoveryprovider.h)
description: Gets the value of the specified query constraint, by name.
helpviewer_keywords: ["Get","Get method","Get method","IProviderQueryConstraintCollection interface","IProviderQueryConstraintCollection interface","Get method","IProviderQueryConstraintCollection.Get","IProviderQueryConstraintCollection::Get","functiondiscoveryprovider/IProviderQueryConstraintCollection::Get","ncd.iproviderqueryconstraintcollection_get"]
old-location: ncd\iproviderqueryconstraintcollection_get.htm
tech.root: ncd
ms.assetid: 30b66ed6-ef02-4a47-baa0-dc48b6d84187
ms.date: 12/05/2018
ms.keywords: Get, Get method, Get method,IProviderQueryConstraintCollection interface, IProviderQueryConstraintCollection interface,Get method, IProviderQueryConstraintCollection.Get, IProviderQueryConstraintCollection::Get, functiondiscoveryprovider/IProviderQueryConstraintCollection::Get, ncd.iproviderqueryconstraintcollection_get
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
 - IProviderQueryConstraintCollection::Get
 - functiondiscoveryprovider/IProviderQueryConstraintCollection::Get
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
 - IProviderQueryConstraintCollection.Get
---

# IProviderQueryConstraintCollection::Get


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the value of the specified query constraint, by name.

## -parameters

### -param pszConstraintName [in]

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
The <i>pszConstraintName</i> or <i>ppszConstraintValue</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderqueryconstraintcollection">IProviderQueryConstraintCollection</a>