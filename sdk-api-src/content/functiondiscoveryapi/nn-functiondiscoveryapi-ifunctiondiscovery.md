---
UID: NN:functiondiscoveryapi.IFunctionDiscovery
title: IFunctionDiscovery (functiondiscoveryapi.h)
description: This interface is used by client programs to discover function instances, get the default function instance for a category, and create advanced Function Discovery query objects that enable registering Function Discovery defaults, among other things.
helpviewer_keywords: ["IFunctionDiscovery","IFunctionDiscovery interface","IFunctionDiscovery interface","described","functiondiscoveryapi/IFunctionDiscovery","ncd.ifunctiondiscovery"]
old-location: ncd\ifunctiondiscovery.htm
tech.root: ncd
ms.assetid: 352a8d61-7d3a-423d-8b7e-1163d4fa1e00
ms.date: 12/05/2018
ms.keywords: IFunctionDiscovery, IFunctionDiscovery interface, IFunctionDiscovery interface,described, functiondiscoveryapi/IFunctionDiscovery, ncd.ifunctiondiscovery
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscovery
 - functiondiscoveryapi/IFunctionDiscovery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionDiscovery
---

# IFunctionDiscovery interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is used by client programs to discover function instances, get the default function instance for a category, and create advanced Function Discovery query objects that enable registering Function Discovery defaults, among other things.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscovery</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscovery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionDiscovery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-addinstance">AddInstance</a>
</td>
<td align="left" width="63%">
Creates or modifies a function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery">CreateInstanceCollectionQuery</a>
</td>
<td align="left" width="63%">
Creates a query for a collection of specific function instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery">CreateInstanceQuery</a>
</td>
<td align="left" width="63%">
Creates a query for a specific function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-getinstance">GetInstance</a>
</td>
<td align="left" width="63%">
Gets the specified function instance, based on identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-getinstancecollection">GetInstanceCollection</a>
</td>
<td align="left" width="63%">
Gets the specified collection of function instances, based on category and subcategory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-removeinstance">RemoveInstance</a>
</td>
<td align="left" width="63%">
Removes the specified function instance, based on category and subcategory.

</td>
</tr>
</table>