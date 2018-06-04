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

# IWSDScopeMatchingRule::GetScopeRule


## -description


Is called to return a URI defining the implemented scope matching rule.


## -parameters




### -param ppszScopeMatchingRule [out]

Pointer to the scope matching rule. The implementor must allocate memory using <a href="https://msdn.microsoft.com/2608985f-56aa-4223-b76d-85ebe3b080fb">WSDAllocateLinkedMemory</a> and the caller must release memory using <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
</table>
 




## -remarks



<b>GetScopeRule</b> should provide a copy of the URI for the scope matching rule this object represents. The copy will be released by the caller using <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.

<i>ppszScopeMatchingRule</i> should never be <b>NULL</b> or an empty string. To register for the <b>NULL</b> scope matching rule, register for the RFC2396 rule as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a>. Probe messages containing a <b>NULL</b> MatchBy value will be converted to RFC2396 before <b>GetScopeRule</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/c608215d-6c72-4567-bf81-15af665e8c52">IWSDScopeMatchingRule</a>
 

 

