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

# IRegTreeItem interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Exposes methods that retrieve and set the state of items in a tree-view control that have the <a href="_win32_Tree_View_Control_Window_Styles">Tree-View Control Window Styles</a> flag set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegTreeItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRegTreeItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRegTreeItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfeff83e-8872-4df2-a519-1335be6e443c">GetCheckState</a>
</td>
<td align="left" width="63%">
Gets the state of a check box item in a tree-view control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba25491-8d18-4040-a256-9078b91e4f3f">SetCheckState</a>
</td>
<td align="left" width="63%">
Sets the state of a check box item in a tree-view control.

</td>
</tr>
</table> 


## -see-also




<a href="_win32_Tree_View_Controls">Tree-View Controls</a>
 

 

