---
UID: NN:wabdefs.IABContainer
title: IABContainer
author: windows-sdk-content
description: Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients.
old-location: wab\_wab_IABContainer.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iabcontainer\iabcontainer.htm
ms.author: windowssdkdev
ms.date: 11/28/2018
ms.keywords: IABContainer, IABContainer interface [Windows Address Book], IABContainer interface [Windows Address Book],described, _wab_IABContainer, wab._wab_IABContainer, wabdefs/IABContainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IABContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IABContainer interface


## -description


Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IABContainer</b> interface inherits from <a href="d83fdd83-3e86-43c8-a73f-8e9e01b53371">IMAPIContainer</a>. <b>IABContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IABContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ee18a71-96a0-4114-a81f-7940f57e67b2">CopyEntries</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa261536-d5d3-41df-bbc9-b1e88c8ecd21">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa09b12c-f0ef-40da-9096-e5d9179b9cfa">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/671dec0b-e7c6-4086-8abf-485796311204">CreateEntry</a>
</td>
<td align="left" width="63%">
Creates a new entry in the address book container.  The WAB supports creation of mail users and distribution lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3576116f-cb53-46f5-b8e0-f7d97dbae5e0">DeleteEntries</a>
</td>
<td align="left" width="63%">
Removes one or more entries from the address book container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8ce57b6-417e-4ee6-b166-f1d21c6376f7">DeleteProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/644dd9c8-7e30-4820-aba1-46d7658e43c9">GetContentsTable</a>
</td>
<td align="left" width="63%">
Retrieves the address of the contents table of the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda1bb0a-606c-4dd7-988c-29ebc67c9673">GetHierarchyTable</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bfb2c59-5b4d-4dc7-a06b-68d0a5429a0a">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee66c9bd-8627-46f2-afd2-0a586ac4f41d">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5d53273-d7fd-4b4a-aab4-4226456e495d">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc52bd78-e43a-4ac3-aec0-88138ca6d2c4">GetPropList</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d841c37a-92db-4608-af3a-fded9bb499ee">GetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1881e19f-9443-4986-8f17-af5faf681ead">GetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9300d757-8eb9-4160-9e05-9eee3b58b0fb">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens a child container object in the open container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9ffd18f-5592-446e-9ec6-33f65c96d66a">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74991ff8-0ec4-413f-ba73-c60c9d0c8065">ResolveNames</a>
</td>
<td align="left" width="63%">
Resolves entries against the address book container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6938680-9dd7-4f30-9667-3d2d8a78ee1c">SaveChanges</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd86662e-c59a-4db4-98f8-19e458ea6eea">SetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee334887-64e7-4746-b151-235ae95cf721">SetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

