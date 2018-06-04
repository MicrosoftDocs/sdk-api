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

# ITfCandidateList interface


## -description


The <b>ITfCandidateList</b> interface is implemented by a text service and is used by the TSF manager or a client (application or other text service) to obtain and manipulate candidate string objects.

The TSF manager implements this interface to provide access to this interface to other clients. This enables the TSF manager to function as a mediator between the client and the text service.

To obtain an instance of this interface the TSF manager or client can call <a href="https://msdn.microsoft.com/ed696088-c599-4c83-968e-d09d9ae81c10">ITfFnReconversion::GetReconversion</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCandidateList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCandidateList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCandidateList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63799a1-2284-4da8-933c-f3616c1cb295">EnumCandidates</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all the candidate string objects in the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cb2127c-cce5-4815-b40b-e6e15058eab5">GetCandidate</a>
</td>
<td align="left" width="63%">
Obtains a specific candidate string object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53b8f8cc-776c-454a-86fa-6fa3b6ac097b">GetCandidateNum</a>
</td>
<td align="left" width="63%">
Obtains the number of candidate string objects in the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcc172f9-4fc3-46f4-a1db-0e75fceafb28">SetResult</a>
</td>
<td align="left" width="63%">
Specifies the result of a reconversion operation for s specific candidate string.

</td>
</tr>
</table> 


## -remarks



When a text service must interpret text before it is inserted into a context, there might be more than one possible interpretation of the text. Speech input is an example of this. If the spoken word is "there", other possible interpretations might be "their" or "they're". The text service will insert the most appropriate text, but there is still some chance of error involved. Text reconversion is the process of allowing the user to select alternate text for the inserted text. The alternate text objects are known as candidates.




## -see-also




<a href="https://msdn.microsoft.com/ed696088-c599-4c83-968e-d09d9ae81c10">ITfFnReconversion::GetReconversion
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

