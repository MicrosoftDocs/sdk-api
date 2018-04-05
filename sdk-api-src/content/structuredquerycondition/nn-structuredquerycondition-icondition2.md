---
UID: NN:structuredquerycondition.ICondition2
title: ICondition2
author: windows-driver-content
description: Extends the functionality of the ICondition interface. ICondition2 provides methods for retrieving information about a search condition.
old-location: search\_search_ICondition2.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\icondition2\icondition2.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ICondition2, ICondition2 interface [search], ICondition2 interface [search], described, _search_ICondition2, search._search_ICondition2, structuredquerycondition/ICondition2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquerycondition.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CONDITION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquerycondition.h
api_name:
-	ICondition2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ICondition2 interface


## -description


Extends the functionality of the <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> interface. <b>ICondition2</b> provides methods for retrieving information about a search condition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICondition2</b> interface inherits from <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>. <b>ICondition2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICondition2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7f3d491-3ddd-4bfe-84e0-a6f3a4c7946d">GetLeafConditionInfo</a>
</td>
<td align="left" width="63%">

          Retrieves the property name, operation, and value from a leaf search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3f9a04f-a596-475d-85f3-b817a54b3e79">GetLocale</a>
</td>
<td align="left" width="63%">

          Retrieves the property name, operation, and value from a leaf search condition node.
        

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting 
condition trees.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<b>Reference</b>
 

 

