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

# IObjectWithFolderEnumMode interface


## -description


Exposes methods that get and set enumeration modes of a parsed item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithFolderEnumMode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectWithFolderEnumMode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithFolderEnumMode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d331255-2295-4f7b-b2d6-1238edcc15bb">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the enumeration mode of the parsed item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e7271ec-47a7-42bf-ab02-26cd587448bd">SetMode</a>
</td>
<td align="left" width="63%">
Sets the enumeration mode of the parsed item.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented as part of a Shell namespace extension, specifically the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
This interface is used by the <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a> method to retrieve the <a href="https://msdn.microsoft.com/ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a">FOLDER_ENUM_MODE</a> value which controls the enumeration mode of the parsed item.

Items with different enumeration modes compare canonically different (SHCIDS_CANONICALONLY) because they enumerate different sets of items.



