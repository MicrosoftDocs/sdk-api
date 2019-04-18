---
UID: NN:functiondiscoveryprovider.IProviderQueryConstraintCollection
title: IProviderQueryConstraintCollection (functiondiscoveryprovider.h)
author: windows-sdk-content
description: This interface is accessible to the provider through the IFunctionDiscoveryProviderQuery::GetQueryConstraints method.
old-location: ncd\iproviderqueryconstraintcollection.htm
tech.root: FunDisc
ms.assetid: 4d8ff5b9-ec4a-4ec6-b133-3d315f9c017b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProviderQueryConstraintCollection, IProviderQueryConstraintCollection interface, IProviderQueryConstraintCollection interface,described, functiondiscoveryprovider/IProviderQueryConstraintCollection, ncd.iproviderqueryconstraintcollection
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
 - IProviderQueryConstraintCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProviderQueryConstraintCollection interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is  accessible to the provider through the <a href="https://msdn.microsoft.com/a8329732-79dd-4606-96c3-40534cde5fc4">IFunctionDiscoveryProviderQuery::GetQueryConstraints</a> method.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderQueryConstraintCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProviderQueryConstraintCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/30b66ed6-ef02-4a47-baa0-dc48b6d84187">Get</a>
</td>
<td align="left" width="63%">
Gets the value of the specified query constraint, by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/401e1723-751a-490b-bcb6-d1e0f2f73dfb">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db8840db-365a-485d-9097-ef98a9d875bc">Item</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified query constraint, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dd03e98-5367-4434-aa68-be36cb7aaf24">Next</a>
</td>
<td align="left" width="63%">
Gets the name and value of the next query  constraint in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56bd143b-b3eb-4273-854b-4d6876ad5e4d">Reset</a>
</td>
<td align="left" width="63%">
Resets the current index to the start of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18c25f6d-387e-46bf-97b6-6bcf195b15e8">Skip</a>
</td>
<td align="left" width="63%">
Skips the next item in the collection.

</td>
</tr>
</table> 

