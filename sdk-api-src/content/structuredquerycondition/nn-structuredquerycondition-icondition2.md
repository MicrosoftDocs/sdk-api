---
UID: NN:structuredquerycondition.ICondition2
title: ICondition2
author: windows-sdk-content
description: Extends the functionality of the ICondition interface. ICondition2 provides methods for retrieving information about a search condition.
old-location: search\_search_ICondition2.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\icondition2\icondition2.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICondition2, ICondition2 interface [search], ICondition2 interface [search],described, _search_ICondition2, search._search_ICondition2, structuredquerycondition/ICondition2
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - ICondition2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICondition2 interface


## -description


Extends the functionality of the <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> interface. <b>ICondition2</b> provides methods for retrieving information about a search condition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICondition2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>. <b>ICondition2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd742807(v=VS.85).aspx">GetLeafConditionInfo</a>
</td>
<td align="left" width="63%">
Retrieves the property name, operation, and value from a leaf search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742808(v=VS.85).aspx">GetLocale</a>
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




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<b>Reference</b>
 

 

