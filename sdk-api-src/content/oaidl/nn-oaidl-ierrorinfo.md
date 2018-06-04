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

# IErrorInfo interface


## -description


Provides detailed contextual error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IErrorInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a textual description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4223508-6e8b-41b7-b808-a0d883bc265b">GetGUID</a>
</td>
<td align="left" width="63%">
Returns the globally unique identifier (GUID) of the interface that defined the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aadfc151-50ed-4a31-b53a-ff9d74dceb6b">GetHelpContext</a>
</td>
<td align="left" width="63%">
Returns the Help context identifier (ID) for the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8458382-0af7-4a9b-add3-9c99af070be4">GetHelpFile</a>
</td>
<td align="left" width="63%">
Returns the path of the Help file that describes the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7bbf4ac-7c02-4abe-83fb-bc9fcd52129e">GetSource</a>
</td>
<td align="left" width="63%">
Returns the language-dependent programmatic ID (ProgID) for the class or application that raised the error.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c258677e-d53e-499d-a414-ce889709b23e">Error Handling Interfaces </a>
 

 

