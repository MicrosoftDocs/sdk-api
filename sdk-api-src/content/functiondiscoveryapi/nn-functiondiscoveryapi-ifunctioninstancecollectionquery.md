---
UID: NN:functiondiscoveryapi.IFunctionInstanceCollectionQuery
title: IFunctionInstanceCollectionQuery (functiondiscoveryapi.h)
description: Implements the asynchronous query for a collection of function instances based on category and subcategory.
old-location: ncd\ifunctioninstancecollectionquery.htm
tech.root: FunDisc
ms.assetid: ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceCollectionQuery, IFunctionInstanceCollectionQuery interface, IFunctionInstanceCollectionQuery interface,described, functiondiscoveryapi/IFunctionInstanceCollectionQuery, ncd.ifunctioninstancecollectionquery
f1_keywords:
- functiondiscoveryapi/IFunctionInstanceCollectionQuery
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
- IFunctionInstanceCollectionQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionInstanceCollectionQuery interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface implements the asynchronous query for a collection of function instances based on category and subcategory. A pointer to this interface is returned when the collection query is created by the client program.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstanceCollectionQuery</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionInstanceCollectionQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionInstanceCollectionQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addpropertyconstraint">AddPropertyConstraint</a>
</td>
<td align="left" width="63%">
Adds a property constraint to the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addqueryconstraint">AddQueryConstraint</a>
</td>
<td align="left" width="63%">
Adds a query constraint to the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a>
</td>
<td align="left" width="63%">
Performs the query defined by <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">CreateInstanceCollectionQuery</a>.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute">Execute</a> method must be invoked by the client program before any data can be retrieved from the query object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>
 

 

