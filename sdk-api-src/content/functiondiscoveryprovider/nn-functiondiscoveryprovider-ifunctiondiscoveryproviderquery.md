---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery
title: IFunctionDiscoveryProviderQuery (functiondiscoveryprovider.h)
description: This interface is passed to all IFunctionDiscoveryProvider::Query method calls and contains query definition information. Providers should use this to determine what the constraints are for each query request they receive.
helpviewer_keywords: ["IFunctionDiscoveryProviderQuery","IFunctionDiscoveryProviderQuery interface","IFunctionDiscoveryProviderQuery interface","described","functiondiscoveryprovider/IFunctionDiscoveryProviderQuery","ncd.ifunctiondiscoveryproviderquery"]
old-location: ncd\ifunctiondiscoveryproviderquery.htm
tech.root: FunDisc
ms.assetid: 97468045-faa5-4690-8db5-50ee9656517b
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProviderQuery, IFunctionDiscoveryProviderQuery interface, IFunctionDiscoveryProviderQuery interface,described, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery, ncd.ifunctiondiscoveryproviderquery
f1_keywords:
- functiondiscoveryprovider/IFunctionDiscoveryProviderQuery
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FunctionDiscoveryProvider.h
api_name:
- IFunctionDiscoveryProviderQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionDiscoveryProviderQuery interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is passed to all <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">IFunctionDiscoveryProvider::Query</a> method calls and contains query definition information.  Providers should use this to determine what the constraints are for each query request they receive. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscoveryProviderQuery</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryProviderQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionDiscoveryProviderQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-getpropertyconstraints">GetPropertyConstraints</a>
</td>
<td align="left" width="63%">
Retrieves the current property constraints.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-getqueryconstraints">GetQueryConstraints</a>
</td>
<td align="left" width="63%">
Retrieves the current query constraints.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-isinstancequery">IsInstanceQuery</a>
</td>
<td align="left" width="63%">
Determines whether a query is for a single function instance or multiple function instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-issubcategoryquery">IsSubcategoryQuery</a>
</td>
<td align="left" width="63%">
Determines whether a query is for function instances in a specific subcategory.

</td>
</tr>
</table> 

