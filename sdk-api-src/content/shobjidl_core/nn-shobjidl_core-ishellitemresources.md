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

# IShellItemResources interface


## -description


Exposes methods to manipulate and query Shell item resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemResources</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellItemResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItemResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b854ee5f-ee4c-49e8-b0de-249154ec9b43">CreateResource</a>
</td>
<td align="left" width="63%">
Creates a specified resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29ac8ac9-4bd1-470c-885a-56f860d50a70">EnumResources</a>
</td>
<td align="left" width="63%">
Gets a resource enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4669ec62-270a-4b75-b073-2f45f11b6f99">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets resource attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5e20d50-510d-4d30-903e-6953846957a9">GetResourceDescription</a>
</td>
<td align="left" width="63%">
Gets a resource description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03e5f9cf-ad5d-487d-bdef-75255a0d1620">GetSize</a>
</td>
<td align="left" width="63%">
Gets the source size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4857b824-2b58-4c26-bbab-8a799d20f584">GetTimes</a>
</td>
<td align="left" width="63%">
Gets file times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15f395a8-70ab-43ba-bb75-6e9b25a19faa">MarkForDelete</a>
</td>
<td align="left" width="63%">
Marks for delete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abef9009-7e0d-4a09-aba8-2b391e4ab487">OpenResource</a>
</td>
<td align="left" width="63%">
Opens a specified resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5112da8-36a0-4b13-b674-c68eab24266d">SetTimes</a>
</td>
<td align="left" width="63%">
Sets file times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4ef7190-0056-423b-b958-bf746a66462d">SupportsResource</a>
</td>
<td align="left" width="63%">
Retrieves whether an item supports a specified resource.

</td>
</tr>
</table> 

