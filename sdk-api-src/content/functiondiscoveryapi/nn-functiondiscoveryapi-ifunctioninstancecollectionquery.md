---
UID: NN:functiondiscoveryapi.IFunctionInstanceCollectionQuery
title: IFunctionInstanceCollectionQuery
author: windows-sdk-content
description: Implements the asynchronous query for a collection of function instances based on category and subcategory.
old-location: ncd\ifunctioninstancecollectionquery.htm
tech.root: FunDisc
ms.assetid: ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFunctionInstanceCollectionQuery, IFunctionInstanceCollectionQuery interface, IFunctionInstanceCollectionQuery interface,described, functiondiscoveryapi/IFunctionInstanceCollectionQuery, ncd.ifunctioninstancecollectionquery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceCollectionQuery interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface implements the asynchronous query for a collection of function instances based on category and subcategory. A pointer to this interface is returned when the collection query is created by the client program.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstanceCollectionQuery</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionInstanceCollectionQuery</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4ff850a8-3208-4fb4-a581-7581e71f34e6">AddPropertyConstraint</a>
</td>
<td align="left" width="63%">
Adds a property constraint to the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/334d7c04-1446-49da-ac45-9a7d4fd82a9d">AddQueryConstraint</a>
</td>
<td align="left" width="63%">
Adds a query constraint to the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a>
</td>
<td align="left" width="63%">
Performs the query defined by <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">CreateInstanceCollectionQuery</a>.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a> method must be invoked by the client program before any data can be retrieved from the query object.




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>
 

 

