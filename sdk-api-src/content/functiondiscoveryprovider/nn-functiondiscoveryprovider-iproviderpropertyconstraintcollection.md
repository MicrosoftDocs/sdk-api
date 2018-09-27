---
UID: NN:functiondiscoveryprovider.IProviderPropertyConstraintCollection
title: IProviderPropertyConstraintCollection
author: windows-sdk-content
description: This interface is accessible to the provider through IFunctionDiscoveryProviderQuery::GetPropertyConstraints.
old-location: ncd\iproviderpropertyconstraintcollection.htm
tech.root: fundisc
ms.assetid: d2e3bc10-e45f-43de-abc5-c5e35d366d87
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IProviderPropertyConstraintCollection, IProviderPropertyConstraintCollection interface, IProviderPropertyConstraintCollection interface,described, functiondiscoveryprovider/IProviderPropertyConstraintCollection, ncd.iproviderpropertyconstraintcollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IProviderPropertyConstraintCollection interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is accessible to the provider through <a href="https://msdn.microsoft.com/d8a45d1b-fb1e-4288-a42a-b967cc9b4533">IFunctionDiscoveryProviderQuery::GetPropertyConstraints</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderPropertyConstraintCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProviderPropertyConstraintCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0388d895-07bb-490c-9fce-0821a51d765a">Get</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified property constraint, by property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62dc9e75-ff40-472f-8acf-ebe40dbac95c">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e5643f6-02a5-48b0-a105-5b82c439b5cc">Item</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified property constraint, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddf9f2b9-92f6-4a1f-86d8-0d9e8c0c4855">Next</a>
</td>
<td align="left" width="63%">
Gets the name and value of the next property constraint in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57357567-b03f-4261-a267-42f44d829d74">Reset</a>
</td>
<td align="left" width="63%">
Resets the current index to the start of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e14bddc-d2ae-41a6-b927-15bdfd3bc598">Skip</a>
</td>
<td align="left" width="63%">
Skips the next item in the collection.

</td>
</tr>
</table> 

