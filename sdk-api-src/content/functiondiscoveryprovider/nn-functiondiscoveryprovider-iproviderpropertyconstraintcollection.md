---
UID: NN:functiondiscoveryprovider.IProviderPropertyConstraintCollection
title: IProviderPropertyConstraintCollection (functiondiscoveryprovider.h)
author: windows-sdk-content
description: This interface is accessible to the provider through IFunctionDiscoveryProviderQuery::GetPropertyConstraints.
old-location: ncd\iproviderpropertyconstraintcollection.htm
tech.root: FunDisc
ms.assetid: d2e3bc10-e45f-43de-abc5-c5e35d366d87
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProviderPropertyConstraintCollection, IProviderPropertyConstraintCollection interface, IProviderPropertyConstraintCollection interface,described, functiondiscoveryprovider/IProviderPropertyConstraintCollection, ncd.iproviderpropertyconstraintcollection
ms.topic: interface
f1_keywords: 
 - "functiondiscoveryprovider/IProviderPropertyConstraintCollection"
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
 - IProviderPropertyConstraintCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProviderPropertyConstraintCollection interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is accessible to the provider through <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-getpropertyconstraints">IFunctionDiscoveryProviderQuery::GetPropertyConstraints</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderPropertyConstraintCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProviderPropertyConstraintCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProviderPropertyConstraintCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-get">Get</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified property constraint, by property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-item">Item</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified property constraint, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-next">Next</a>
</td>
<td align="left" width="63%">
Gets the name and value of the next property constraint in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the current index to the start of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the next item in the collection.

</td>
</tr>
</table> 

