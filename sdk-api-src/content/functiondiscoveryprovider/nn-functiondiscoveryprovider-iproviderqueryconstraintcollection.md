---
UID: NN:functiondiscoveryprovider.IProviderQueryConstraintCollection
title: IProviderQueryConstraintCollection (functiondiscoveryprovider.h)
description: This interface is accessible to the provider through the IFunctionDiscoveryProviderQuery::GetQueryConstraints method.
helpviewer_keywords: ["IProviderQueryConstraintCollection","IProviderQueryConstraintCollection interface","IProviderQueryConstraintCollection interface","described","functiondiscoveryprovider/IProviderQueryConstraintCollection","ncd.iproviderqueryconstraintcollection"]
old-location: ncd\iproviderqueryconstraintcollection.htm
tech.root: ncd
ms.assetid: 4d8ff5b9-ec4a-4ec6-b133-3d315f9c017b
ms.date: 12/05/2018
ms.keywords: IProviderQueryConstraintCollection, IProviderQueryConstraintCollection interface, IProviderQueryConstraintCollection interface,described, functiondiscoveryprovider/IProviderQueryConstraintCollection, ncd.iproviderqueryconstraintcollection
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
 - IProviderQueryConstraintCollection
 - functiondiscoveryprovider/IProviderQueryConstraintCollection
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
 - IProviderQueryConstraintCollection
---

# IProviderQueryConstraintCollection interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is  accessible to the provider through the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-getqueryconstraints">IFunctionDiscoveryProviderQuery::GetQueryConstraints</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderQueryConstraintCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProviderQueryConstraintCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProviderQueryConstraintCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-get">Get</a>
</td>
<td align="left" width="63%">
Gets the value of the specified query constraint, by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-item">Item</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified query constraint, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-next">Next</a>
</td>
<td align="left" width="63%">
Gets the name and value of the next query  constraint in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the current index to the start of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the next item in the collection.

</td>
</tr>
</table>

