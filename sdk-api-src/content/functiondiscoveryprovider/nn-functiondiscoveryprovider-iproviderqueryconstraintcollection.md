---
UID: NN:functiondiscoveryprovider.IProviderQueryConstraintCollection
title: IProviderQueryConstraintCollection
author: windows-driver-content
description: This interface is accessible to the provider through the IFunctionDiscoveryProviderQuery::GetQueryConstraints method.
old-location: ncd\iproviderqueryconstraintcollection.htm
old-project: FunDisc
ms.assetid: 4d8ff5b9-ec4a-4ec6-b133-3d315f9c017b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IProviderQueryConstraintCollection, IProviderQueryConstraintCollection interface, IProviderQueryConstraintCollection interface, described, functiondiscoveryprovider/IProviderQueryConstraintCollection, ncd.iproviderqueryconstraintcollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PropertyConstraint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FunctionDiscoveryProvider.h
api_name:
-	IProviderQueryConstraintCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets the value of the specified query constraint, by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Gets the name and value of the specified query constraint, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Gets the name and value of the next query  constraint in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the current index to the start of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips the next item in the collection.

</td>
</tr>
</table> 

