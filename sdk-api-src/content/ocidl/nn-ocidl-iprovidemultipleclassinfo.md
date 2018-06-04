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

# IProvideMultipleClassInfo interface


## -description


An extension to <a href="https://msdn.microsoft.com/e62785e4-994c-48cc-b5b9-7ec2b07c9d63">IProvideClassInfo2</a> that makes it faster and easier to retrieve type information from a component that may have multiple coclasses that determine its behavior. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideMultipleClassInfo</b> interface inherits from <b>IProvideClassInfo2</b>. <b>IProvideMultipleClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProvideMultipleClassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/084dfb9d-5545-4845-9959-1b054566adca">GetInfoOfIndex</a>
</td>
<td align="left" width="63%">
Retrieves the type information from the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16b456fe-70d2-47cd-83b8-bc9b1f8a2aaa">GetMultiTypeInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of type information blocks that this object must provide.

</td>
</tr>
</table> 

