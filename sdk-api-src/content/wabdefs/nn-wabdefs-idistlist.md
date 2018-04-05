---
UID: NN:wabdefs.IDistList
title: IDistList
author: windows-driver-content
description: Do not use. This interface is used to provide access to distribution lists in modifiable address book containers. The interface provides methods to create, copy, and delete distribution lists, in addition to performing name resolution.
old-location: wab\_wab_IDistList.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\idistlist\idistlist.htm
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: IDistList, IDistList interface [Windows Address Book], IDistList interface [Windows Address Book], described, _wab_IDistList, wab._wab_IDistList, wabdefs/IDistList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wabdefs.h
req.include-header: Wabtmp.h
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
req.typenames: WABIMPORTPARAM, *LPWABIMPORTPARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wab32.dll
api_name:
-	IDistList
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll
req.irql: 
req.product: Internet Explorer 4.0
---

# IDistList interface


## -description


Do not use. This interface is used to provide access to distribution lists in modifiable address book containers. The interface provides methods to create, copy, and delete distribution lists, in addition to performing name resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDistList</b> interface inherits from <a href="d83fdd83-3e86-43c8-a73f-8e9e01b53371">IMAPIContainer</a>. <b>IDistList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDistList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ee71017-fd4c-4c7f-9c0e-d69d9a313963">CopyEntries</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17e13b19-2477-42d9-9e58-92c4d993a6b9">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/264f2f5f-74fe-4c96-afc5-a44fb8883cdf">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b159ccd3-5825-4e1b-acd0-9287b46ea69e">CreateEntry</a>
</td>
<td align="left" width="63%">
Creates a new entry in the distribution list container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d268a7c-7a93-4155-b2cb-a1b1067a8ec6">DeleteEntries</a>
</td>
<td align="left" width="63%">
Removes one or more entries from the distribution list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d794098c-28b3-4e80-8319-54e39aa0199d">DeleteProps</a>
</td>
<td align="left" width="63%">
Deletes property values from a distribution list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f276c58a-4887-4cde-ba1e-a743a6cb4ea3">GetContentsTable</a>
</td>
<td align="left" width="63%">
Retrieves the address of the contents table of the distribution list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d92f720-86dd-46a2-ac95-1a75f1dd3959">GetHierarchyTable</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cea7449-8722-4587-b31b-b9563271d831">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Retrieves the property identifiers that correspond to one or more property names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/878d3d3e-94a9-4e62-beec-1c745f1fd2c5">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b881a917-d171-441f-b8b3-6aa0261c5940">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/509a7a2e-41a4-49b5-bd16-c747a99932ea">GetPropList</a>
</td>
<td align="left" width="63%">
Retrieves a list of the object property tags.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e694aa2-2954-4554-9d99-1b3cc8510513">GetProps</a>
</td>
<td align="left" width="63%">
Retrieves the property tag information for the distribution list items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbe786b2-0cde-457f-a5a2-29107bf340e7">GetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02d46f4b-d511-4fe9-b995-bcd985b711e2">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens an entry from the distribution list and returns a pointer to the object to provide further access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f49de61-7010-4ee3-9597-327e0db5fc99">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ed050c6-3b37-429b-b328-5df220f38e84">ResolveNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b1cb381-8b8b-456e-a139-aa550129f983">SaveChanges</a>
</td>
<td align="left" width="63%">
Provides the ability to save changes to the open distribution list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cfd22b1-19cb-48e3-a51f-b1a1437e61a3">SetProps</a>
</td>
<td align="left" width="63%">
Sets property values for a distribution list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5295a39-4ac1-404c-9cd6-854b0581f23f">SetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

