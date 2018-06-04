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

# ISpellChecker2 interface


## -description


Represents a particular spell checker for a particular language, with the added ability to remove words from the added words dictionary, or from the ignore list.

The <b>ISpellChecker2</b> can also be used to check text, get suggestions, update user dictionaries, and maintain options, as can <a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a> from which it is derived.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellChecker2</b> interface inherits from <a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>. <b>ISpellChecker2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpellChecker2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a word that was previously added by <a href="https://msdn.microsoft.com/d600a57e-7191-4a82-8004-026a04ef94ed">ISpellChecker.Add</a>, or set by <a href="https://msdn.microsoft.com/e82dd7a3-3ec4-4ef4-a19f-ad44866bbb1c">ISpellChecker.Ignore</a> to be ignored.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>
 

 

