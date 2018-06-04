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

# IDefaultExtractIconInit interface


## -description


Exposes methods to set default icons associated with an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDefaultExtractIconInit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDefaultExtractIconInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDefaultExtractIconInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a834c1e-602a-4736-8807-7dd04c6dc5c2">SetDefaultIcon</a>
</td>
<td align="left" width="63%">
Sets the default icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Sets GIL_XXX flags. See <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dce75b90-f569-4983-a540-82a021377287">SetKey</a>
</td>
<td align="left" width="63%">
Sets the registry key from which to load the "DefaultIcon" value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49d11767-4237-48f3-973b-03cf032c5e68">SetNormalIcon</a>
</td>
<td align="left" width="63%">
Sets the normal icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/837a0006-2153-405f-a035-06738b89b058">SetOpenIcon</a>
</td>
<td align="left" width="63%">
Sets the icon that allows containers to specify an "open" look.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1defab08-3dce-4668-aca3-d11821a4c339">SetShortcutIcon</a>
</td>
<td align="left" width="63%">
Sets the icon for a shortcut to the object.

</td>
</tr>
</table> 

