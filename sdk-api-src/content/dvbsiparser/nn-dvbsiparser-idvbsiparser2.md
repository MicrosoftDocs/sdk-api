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

# IDvbSiParser2 interface


## -description



The <b>IDvbSiParser2</b> interface retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSiParser2</b> interface inherits from <a href="https://msdn.microsoft.com/092162af-5f88-4ce5-ac2f-89327f094804">IDvbSiParser</a>. <b>IDvbSiParser2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbSiParser2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47ccce59-d67e-4994-b69d-8dac425b375a">GetEIT2</a>
</td>
<td align="left" width="63%">
Gets the event information table (EIT).

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <b>CoCreateInstance</b>. Use the following CLSID:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>F6B96EDA-1A94-4476-A85F-4D3DC7B39C3F</pre>
</td>
</tr>
</table></span></div>
This CLSID is not is not published in an SDK header; define a new GUID constant in your application.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/092162af-5f88-4ce5-ac2f-89327f094804">IDvbSiParser</a>
 

 

