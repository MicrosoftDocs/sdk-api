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

# IComprehensiveSpellCheckProvider interface


## -description


Allows the provider to optionally support a more comprehensive spell checking functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComprehensiveSpellCheckProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComprehensiveSpellCheckProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComprehensiveSpellCheckProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD334EB8-4E14-478D-AB2A-E7F863C4BE0F">ComprehensiveCheck</a>
</td>
<td align="left" width="63%">
Spell-check the provider text in a more thorough manner than <a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>.

</td>
</tr>
</table> 

