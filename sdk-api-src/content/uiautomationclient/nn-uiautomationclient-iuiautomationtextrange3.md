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

# IUIAutomationTextRange3 interface


## -description


Extends the <a href="https://msdn.microsoft.com/62E95500-5691-FAE8-BC31-0BB31318D8A4">IUIAutomationTextRange2</a> interface to support faster access to the underlying rich text data on a text range.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRange3</b> interface inherits from <a href="https://msdn.microsoft.com/62E95500-5691-FAE8-BC31-0BB31318D8A4">IUIAutomationTextRange2</a>. <b>IUIAutomationTextRange3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextRange3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1AF29BF1-A074-4054-B338-7B6922B1415C">GetAttributeValues</a>
</td>
<td align="left" width="63%">
Returns all of the requested text attribute values for a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/7a77774e-7be0-473e-a0c9-e1aa108549e1">GetAttributeValue</a>, except it can retrieve multiple values instead of just one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1C8F0E81-ED73-4752-BD27-7981508671D0">GetChildrenBuildCache</a>
</td>
<td align="left" width="63%">
Returns the children and supplied properties and patterns for elements in a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/714e9d91-c6b9-4fa2-8a14-9bdd721b3135">GetChildren</a>, but adds the standard build cache pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F5BC5DB-F9C0-40DF-8E29-FFACFBCAD80F">GetEnclosingElementBuildCache</a>
</td>
<td align="left" width="63%">
Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/0120b4af-6f08-4bbd-b649-0f8e84cda3b9">GetEnclosingElement</a>, but adds the standard build cache pattern.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/62E95500-5691-FAE8-BC31-0BB31318D8A4">IUIAutomationTextRange2</a>
 

 

