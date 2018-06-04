---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IQuerySolution interface


## -description



          Provides methods that retrieve information about the interpretation of a parsed query.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQuerySolution</b> interface inherits from <a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>. <b>IQuerySolution</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQuerySolution</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50eead1a-5eb9-4bc9-ba54-c6dc77284f4d">GetErrors</a>
</td>
<td align="left" width="63%">

          Identifies parts of the input string that the parser did not recognize or did not use when constructing the <b>IQuerySolution</b> condition tree.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c615e9c-0e15-475d-831f-3bbb896c6e85">GetLexicalData</a>
</td>
<td align="left" width="63%">

          Reports the query string, how it was tokenized, and what LCID and word breaker were used to parse it.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef03828a-ac31-4e73-a8bb-44f0b1963107">GetQuery</a>
</td>
<td align="left" width="63%">

          Retrieves the condition tree and the semantic type of the solution.
        

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.



