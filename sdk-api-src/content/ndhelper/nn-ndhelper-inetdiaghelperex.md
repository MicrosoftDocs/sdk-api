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

# INetDiagHelperEx interface


## -description


The <b>INetDiagHelperEx</b> interface provides methods that extend on the <a href="https://msdn.microsoft.com/7f1b8a5b-389b-4276-a49d-94a39be3c35c">INetDiagHelper</a> interface to capture and provide information associated with diagnoses and resolution of network-related issues.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetDiagHelperEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetDiagHelperEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetDiagHelperEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ac1c901-cfc3-4ef6-aceb-d496179145b8">INetDiagHelperEx::ReconfirmLowHealth</a>
</td>
<td align="left" width="63%">
Adds a second Low Health pass after hypotheses have been diagnosed and before repairs are retrieved. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a85e375b-78f3-494b-846e-8ea5dd4b5b37">INetDiagHelperEx::ReproduceFailure</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdc3cdd5-c301-4052-81ec-a4a68248d3a4">INetDiagHelperEx::SetUtilities</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7f1b8a5b-389b-4276-a49d-94a39be3c35c">INetDiagHelper</a>
 

 

