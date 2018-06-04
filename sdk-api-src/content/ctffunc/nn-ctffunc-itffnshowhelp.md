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

# ITfFnShowHelp interface


## -description


The <b>ITfFnShowHelp</b> interface is implemented by a text service to enable the language bar to place a help command for the text service in the language bar help menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnShowHelp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnShowHelp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnShowHelp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e150dffe-4a02-4d16-9017-f86111970aea">Show</a>
</td>
<td align="left" width="63%">
Called when the user selects a text service help menu item.

</td>
</tr>
</table> 


## -remarks



The TSF manager obtains this interface from the text service by calling the text service <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnShowHelp.

The TSF manager obtains the help menu text by calling the text service's <a href="https://msdn.microsoft.com/da52ca6d-9606-45c5-8db9-c876c827df14">ITfFunction::GetDisplayName</a>.




## -see-also




<a href="https://msdn.microsoft.com/140b1ed8-8876-4f06-8ed2-7b0dccdc0a69">ITfFunction
      </a>



<a href="https://msdn.microsoft.com/da52ca6d-9606-45c5-8db9-c876c827df14">
        ITfFunction::GetDisplayName
      </a>



<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">
        ITfFunctionProvider::GetFunction
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

