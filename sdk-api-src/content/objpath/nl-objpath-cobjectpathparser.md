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

# CObjectPathParser class


## -description


<p class="CCE_Message">[The <b>CObjectPathParser</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Parses a WMI path which can include a remote computer name, namespaces, and classes. Use of this object is not recommended. Instead, use the <a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a> COM interface.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CObjectPathParser</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CObjectPathParser</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aeb162a-8e93-4a2f-9609-693a26027a44">CObjectPathParser</a>
</td>
<td align="left" width="63%">
Constructs and initializes an instance of a <b>CObjectPathParser</b> object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CObjectPathParser</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9164d7b2-15b8-4b73-ab8c-68ed45692ea0">Free</a>
</td>
<td align="left" width="63%">Overloaded. Releases the memory that contains the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c39dbef5-9050-487a-8e06-17087753330d">Parse</a>
</td>
<td align="left" width="63%">
Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6135b808-b9eb-4ba0-9eb8-e7a59993ae34">UnParse</a>
</td>
<td align="left" width="63%">
Converts a structure that contains the parsed path to a string.

</td>
</tr>
</table> 


## -members

The <b>CObjectPathParser</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9164d7b2-15b8-4b73-ab8c-68ed45692ea0">Free</a>
</td>
<td align="left" width="63%">Overloaded. Releases the memory that contains the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c39dbef5-9050-487a-8e06-17087753330d">Parse</a>
</td>
<td align="left" width="63%">
Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6135b808-b9eb-4ba0-9eb8-e7a59993ae34">UnParse</a>
</td>
<td align="left" width="63%">
Converts a structure that contains the parsed path to a string.

</td>
</tr>
</table>Releases the memory that contains the path.

Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others.

Converts a structure that contains the parsed path to a string.

 

