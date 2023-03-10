---
UID: NF:functiondiscoveryprovider.IProviderPropertyConstraintCollection.GetCount
title: IProviderPropertyConstraintCollection::GetCount (functiondiscoveryprovider.h)
description: Gets the number of items in the collection. (IProviderPropertyConstraintCollection.GetCount)
helpviewer_keywords: ["GetCount","GetCount method","GetCount method","IProviderPropertyConstraintCollection interface","IProviderPropertyConstraintCollection interface","GetCount method","IProviderPropertyConstraintCollection.GetCount","IProviderPropertyConstraintCollection::GetCount","functiondiscoveryprovider/IProviderPropertyConstraintCollection::GetCount","ncd.iproviderpropertyconstraintcollection_getcount"]
old-location: ncd\iproviderpropertyconstraintcollection_getcount.htm
tech.root: ncd
ms.assetid: 62dc9e75-ff40-472f-8acf-ebe40dbac95c
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method, GetCount method,IProviderPropertyConstraintCollection interface, IProviderPropertyConstraintCollection interface,GetCount method, IProviderPropertyConstraintCollection.GetCount, IProviderPropertyConstraintCollection::GetCount, functiondiscoveryprovider/IProviderPropertyConstraintCollection::GetCount, ncd.iproviderpropertyconstraintcollection_getcount
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
 - IProviderPropertyConstraintCollection::GetCount
 - functiondiscoveryprovider/IProviderPropertyConstraintCollection::GetCount
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
 - IProviderPropertyConstraintCollection.GetCount
---

# IProviderPropertyConstraintCollection::GetCount


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the number of items in the collection.

## -parameters

### -param pdwCount [out]

The number of items.

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
</table>

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderpropertyconstraintcollection">IProviderPropertyConstraintCollection</a>
