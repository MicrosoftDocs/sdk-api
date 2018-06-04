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

# ILanguageExceptionErrorInfo2 interface


## -description


Enables language projections to provide and retrieve error information as with <a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>, with the additional benefit of working across language boundaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageExceptionErrorInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>. <b>ILanguageExceptionErrorInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageExceptionErrorInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60026962-4E6C-4906-97D9-46BD2BCA3AC6">CapturePropagationContext</a>
</td>
<td align="left" width="63%">
Captures the context of an exception across a language boundary and across threads.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10A45EF1-AF8F-498D-B95B-FCE9EF8AB203">GetPreviousLanguageExceptionErrorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the previous language exception error information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E5C74AE-C8C6-4D95-A836-DD47E50CF25D">GetPropagationContextHead</a>
</td>
<td align="left" width="63%">
Retrieves the propagation context head.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>
 

 

