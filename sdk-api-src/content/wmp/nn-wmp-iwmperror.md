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

# IWMPError interface


## -description



The <b>IWMPError</b> interface provides methods for accessing a collection of <b>IWMPErrorItem</b> pointers.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPError</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c965b48-d178-4b41-add7-0b7d208380a3">clearErrorQueue</a>
</td>
<td align="left" width="63%">
Clears the errors from the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ad21e08-4566-4f3a-8506-308432996481">get_errorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of errors in the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fda2f53-e8d8-4b67-9aa1-72273fc68f6c">get_item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPErrorItem</b> interface at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98ece2f3-36c4-4bb2-9a06-c3ce57cbcbe7">webHelp</a>
</td>
<td align="left" width="63%">
Launches the Microsoft Windows Media Player Web Help page to display further information about the error.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPError</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/db00797b-989f-4f92-8fac-aaa147e37383">get_error</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4675eebf-80d7-4412-b3f1-ec54b977db31">IWMPErrorItem Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

