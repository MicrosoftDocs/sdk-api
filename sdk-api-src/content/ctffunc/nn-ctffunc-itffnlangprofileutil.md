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

# ITfFnLangProfileUtil interface


## -description


The <b>ITfFnLangProfileUtil</b> interface is implemented by the speech text service and used to provide utility methods for the speech text service. A text service can create an instance of this interface by calling CoCreateInstance with CLSID_SapiLayr and IID_ITfFnLangProfileUtil.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnLangProfileUtil</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnLangProfileUtil</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnLangProfileUtil</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0525a1b-e23c-49af-954d-e2d190c2f520">IsProfileAvailableForLang</a>
</td>
<td align="left" width="63%">
Determines if the speech text service has a profile available for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b86206d-a299-4207-a0be-35a334786560">RegisterActiveProfiles</a>
</td>
<td align="left" width="63%">
Causes the speech text service to register its active profiles.

</td>
</tr>
</table> 

